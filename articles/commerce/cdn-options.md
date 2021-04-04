---
title: İçerik teslimi ağı uygulama seçenekleri
description: Bu konu, Microsoft Dynamics 365 Commerce ortamlarıyla kullanılabilecek içerik teslim ağı (CDN) uygulaması için farklı seçenekleri inceler. Bu seçenekler arasında, yerel, Commerce tarafından sağlanan Azure Front Door örnekleri ve müşterilere ait Azure Front Door örnekleri bulunur.
author: BrianShook
manager: AnnBe
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ae0769b7e19f80244186c51454444c499c5e497f
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582815"
---
# <a name="content-delivery-network-implementation-options"></a><span data-ttu-id="f5c29-104">İçerik teslimi ağı uygulama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="f5c29-104">Content delivery network implementation options</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5c29-105">Bu konu, Microsoft Dynamics 365 Commerce ortamlarıyla kullanılabilecek içerik teslim ağı (CDN) uygulaması için farklı seçenekleri inceler.</span><span class="sxs-lookup"><span data-stu-id="f5c29-105">This topic reviews the different options for content delivery network (CDN) implementation that can be used with Microsoft Dynamics 365 Commerce environments.</span></span> <span data-ttu-id="f5c29-106">Bu seçenekler arasında, yerel, Commerce tarafından sağlanan Azure Front Door örnekleri ve müşterilere ait Azure Front Door örnekleri bulunur.</span><span class="sxs-lookup"><span data-stu-id="f5c29-106">These options include native, Commerce-provided instances of Azure Front Door and customer-owned instances of Azure Front Door.</span></span>

<span data-ttu-id="f5c29-107">Commerce müşterilerinin, Commerce ortamlarıyla hangi CDN hizmetini kullanacaklarını düşündüklerinde çeşitli seçenekleri vardır.</span><span class="sxs-lookup"><span data-stu-id="f5c29-107">Commerce customers have several options when they are considering which CDN service to use with their Commerce environment.</span></span> <span data-ttu-id="f5c29-108">Commerce temel barındırma ve özel etki alanı gereksinimlerini kapsayan temel Azure Front Door desteği ile sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="f5c29-108">Commerce is released with basic Azure Front Door support that covers basic hosting and custom domain requirements.</span></span> <span data-ttu-id="f5c29-109">Web uygulaması güvenlik duvarı (WAF) gibi daha fazla denetim ve daha fazla belirli güvenlik becerileri isteyen şirketler için en iyi seçenek, Azure Front Door'un müşteriye ait bir örneğini veya harici bir CDN hizmeti kullanmak olabilir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-109">For companies that want more control and more specific security abilities, such as a web application firewall (WAF), the best option might be to use either a customer-owned instance of Azure Front Door or an external CDN service.</span></span>

<span data-ttu-id="f5c29-110">Commerce ortamlarıyla aşağıdaki üç CDN uygulama seçeneği kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="f5c29-110">The following three CDN implementation options can be used with Commerce environments:</span></span>

- <span data-ttu-id="f5c29-111">Commerce tarafından sağlanan Azure Front Door örneği</span><span class="sxs-lookup"><span data-stu-id="f5c29-111">The Commerce-provided instance of Azure Front Door</span></span>
- <span data-ttu-id="f5c29-112">Müşteriye ait Azure Front Door örneği (Artırılmış denetim ve ek güvenlik özellikleri için)</span><span class="sxs-lookup"><span data-stu-id="f5c29-112">A customer-owned instance of Azure Front Door (for increased control and additional security features)</span></span>
- <span data-ttu-id="f5c29-113">Harici bir CDN hizmeti</span><span class="sxs-lookup"><span data-stu-id="f5c29-113">An external CDN service</span></span>

<span data-ttu-id="f5c29-114">Üç CDN uygulama seçeneği de özel etki alanlarından yalnızca dinamik HTML içeriği sunar.</span><span class="sxs-lookup"><span data-stu-id="f5c29-114">All three CDN implementation options deliver only dynamic HTML content from custom domains.</span></span> <span data-ttu-id="f5c29-115">Commerce, tüm JavaScript, Geçişli stil sayfaları (CSS), görüntü, video ve diğer statik içeriği Microsoft tarafından yönetilen CDN'ler aracılığıyla otomatik olarak işler.</span><span class="sxs-lookup"><span data-stu-id="f5c29-115">Commerce automatically handles all JavaScript, Cascading Style Sheets (CSS), images, video, and other static content through Microsoft-managed CDNs.</span></span> <span data-ttu-id="f5c29-116">Seçtiğiniz seçenek, işlevsel özellikleri, kontrol özelliklerini ve kullanılabilen ek güvenlik özelliklerini belirler.</span><span class="sxs-lookup"><span data-stu-id="f5c29-116">The option that you choose determines the operational capabilities, control capabilities, and additional security capabilities that are available.</span></span>

<span data-ttu-id="f5c29-117">Aşağıdaki örnekte Commerce mimarisine genel bakış verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-117">The following illustration shows an overview of the Commerce architecture.</span></span>

![Commerce mimarisine genel bakış](media/Commerce_CDN-Option_ComparisonModels.png)

<span data-ttu-id="f5c29-119">Commerce siteniz için bir Azure Front Door örneği ayarlama hakkında daha fazla bilgi için bkz. [CDN Desteği ekleme](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="f5c29-119">For more information about how to set up an instance of Azure Front Door for your Commerce site, see [Add CDN Support](add-cdn-support.md).</span></span>

## <a name="use-the-commerce-provided-azure-front-door-instance"></a><span data-ttu-id="f5c29-120">Commerce tarafından sağlanan Azure Front Door örneğini kullanma</span><span class="sxs-lookup"><span data-stu-id="f5c29-120">Use the Commerce-provided Azure Front Door instance</span></span>

<span data-ttu-id="f5c29-121">Aşağıdaki tabloda içerik bitiş noktalarını yönetmek üzere, Commerce tarafından sağlanan Azure Front Door örneğini kullanmanın avantajları ve dezavantajları listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-121">The following table lists the pros and cons of using the Commerce-provided instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="f5c29-122">Avantajlar</span><span class="sxs-lookup"><span data-stu-id="f5c29-122">Pros</span></span> | <span data-ttu-id="f5c29-123">Dezavantajlar</span><span class="sxs-lookup"><span data-stu-id="f5c29-123">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="f5c29-124">Örnek, Commerce maliyetine dahildir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-124">The instance is included in the Commerce cost.</span></span></li><li><span data-ttu-id="f5c29-125">Örnek Commerce ekibi tarafından yönetildiğinden, daha az bakım gerektirir ve paylaşılan kurulum adımları vardır.</span><span class="sxs-lookup"><span data-stu-id="f5c29-125">Because the instance is managed by the Commerce team, less maintenance is required, and there are shared setup steps.</span></span></li><li><span data-ttu-id="f5c29-126">Azure'da barındırılan altyapı ölçeklenebilir, güvenli ve güvenilirdir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-126">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="f5c29-127">Güvenli Yuva Katmanı (SSL) sertifikası bir kerelik kurulum gerektirir ve otomatik olarak yenilenir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-127">The Secure Sockets Layer (SSL) certificate requires a one-time setup and is automatically renewed.</span></span></li><li><span data-ttu-id="f5c29-128">Örnek, Commerce ekibi tarafından hatalar ve bozukluklar için izlenir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-128">The instance is monitored for errors and anomalies by the Commerce team.</span></span></li></ul> | <ul><li><span data-ttu-id="f5c29-129">WAF desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="f5c29-129">A WAF isn't supported.</span></span></li><li><span data-ttu-id="f5c29-130">Belirli özelleştirmeler veya ayar ayarlamaları yoktur.</span><span class="sxs-lookup"><span data-stu-id="f5c29-130">There are no specific customizations or setting adjustments.</span></span></li><li><span data-ttu-id="f5c29-131">Örnek, güncelleştirmeler veya değişiklikler için Commerce ekibine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f5c29-131">The instance depends on the Commerce team for updates or changes.</span></span></li><li><span data-ttu-id="f5c29-132">Apex etki alanları için ayrı bir Azure Front Door örneği gereklidir ve Apex etki alanlarını Azure DNS ile bütünleştirmek için ek işler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-132">A separate Azure Front Door instance is required for apex domains, and extra work is required to integrate apex domains with Azure DNS.</span></span></li><li><span data-ttu-id="f5c29-133">Müşteriye saniyedeki yanıtlar (RPS) veya hata oranı hakkında hiçbir telemetri sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="f5c29-133">No telemetry about responses per second (RPS) or the error rate is provided to the customer.</span></span></li></ul> |

<span data-ttu-id="f5c29-134">Aşağıdaki resimde, Commerce tarafından sağlanan Azure Front Door örneğinin mimarisi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-134">The following illustration shows the architecture of the Commerce-provided Azure Front Door instance.</span></span>

![Commerce tarafından sağlanan Azure Front Door örneği](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a><span data-ttu-id="f5c29-136">Müşteriye ait bir Azure Front Door örneği kullanma</span><span class="sxs-lookup"><span data-stu-id="f5c29-136">Use a customer-owned Azure Front Door instance</span></span>

<span data-ttu-id="f5c29-137">Aşağıdaki tabloda içerik bitiş noktalarını yönetmek üzere, müşteriye ait Azure Front Door örneğini kullanmanın avantajları ve dezavantajları listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-137">The following table lists the pros and cons of using a customer-owned instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="f5c29-138">Avantajlar</span><span class="sxs-lookup"><span data-stu-id="f5c29-138">Pros</span></span> | <span data-ttu-id="f5c29-139">Dezavantajlar</span><span class="sxs-lookup"><span data-stu-id="f5c29-139">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="f5c29-140">Kurulum güvenli ve yönetilmesi kolaydır.</span><span class="sxs-lookup"><span data-stu-id="f5c29-140">Setup is secure and easy to manage.</span></span></li><li><span data-ttu-id="f5c29-141">Azure'da barındırılan altyapı ölçeklenebilir, güvenli ve güvenilirdir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-141">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="f5c29-142">Örnek, WAF tümleştirmesine ve özellikle sitenize göre ayarlanmış daha hassas güvenlik sağlayan detaylı kural denetimlerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="f5c29-142">The instance allows for WAF integration and granular rule controls for finer-grade security that is tuned specifically for your site.</span></span></li><li><span data-ttu-id="f5c29-143">Örnek, SSL sertifikalarının (hem müşteriye ait hem de Azure Front Door'un yönettiği) ve etki alanı bağlamanın daha iyi denetimine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="f5c29-143">The instance allows for finer control of SSL certificates (both customer-owned and Azure Front Door–managed) and domain linking.</span></span></li><li><span data-ttu-id="f5c29-144">Örnek doğrudan Azure DNS ile eşlendiyse, bir Apex etki alanı çözümü sunar.</span><span class="sxs-lookup"><span data-stu-id="f5c29-144">The instance offers an apex domain solution if it's paired directly with Azure DNS.</span></span></li><li><span data-ttu-id="f5c29-145">Telemetri ve uyarı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="f5c29-145">Telemetry and alerting are provided.</span></span></li><li><span data-ttu-id="f5c29-146">SSL sertifikası bir kerelik kurulum gerektirir ve otomatik olarak yenilenir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-146">The SSL certificate requires a one-time setup and is automatically renewed.</span></span></li></ul> | <ul><li><span data-ttu-id="f5c29-147">Örnek kendi kendine yönetilir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-147">The instance is self-managed.</span></span></li><li><span data-ttu-id="f5c29-148">Öğrenme ve alışma süresi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-148">Initial knowledge ramp-up is required.</span></span></li></ul> |

<span data-ttu-id="f5c29-149">Aşağıdaki resimde, müşteriye ait bir Azure Front Door örneği içeren bir Commerce altyapısı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-149">The following illustration shows a Commerce infrastructure that includes a customer-owned Azure Front Door instance.</span></span>

![Müşteriye ait bir Azure Front Door örneği içeren bir Commerce altyapısı](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a><span data-ttu-id="f5c29-151">Harici bir CDN hizmeti kullanma</span><span class="sxs-lookup"><span data-stu-id="f5c29-151">Use an external CDN service</span></span>

<span data-ttu-id="f5c29-152">Aşağıdaki tabloda içerik son noktalarını yönetmek için harici bir CDN hizmeti kullanmanın avantajları ve dezavantajları listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-152">The following table lists the pros and cons of using an external CDN service to manage content endpoints.</span></span>

| <span data-ttu-id="f5c29-153">Avantajlar</span><span class="sxs-lookup"><span data-stu-id="f5c29-153">Pros</span></span> | <span data-ttu-id="f5c29-154">Dezavantajlar</span><span class="sxs-lookup"><span data-stu-id="f5c29-154">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="f5c29-155">Bu seçenek, varolan etki alanı zaten harici bir CDN'de barındırılıyorsa yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="f5c29-155">This option is useful when the existing domain is already hosted on an external CDN.</span></span></li><li><span data-ttu-id="f5c29-156">Rakip CDN'ler (örneğin, Akamai) daha fazla WAF özelliğine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-156">Competitor CDNs (for example, Akamai) might have more WAF capabilities.</span></span></li></ul> | <ul><li><span data-ttu-id="f5c29-157">Ayrı bir sözleşme ve ek maliyetlendirme gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-157">A separate contract and additional costing are required.</span></span></li><li><span data-ttu-id="f5c29-158">SSL ek maliyet gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-158">SSL might incur additional costs.</span></span></li><li><span data-ttu-id="f5c29-159">Hizmet Azure bulut yapısından ayrı olduğundan, ek altyapı yönetilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-159">Because the service is separate from the Azure cloud structure, additional infrastructure must be managed.</span></span></li><li><span data-ttu-id="f5c29-160">Bu hizmet uç noktada ve güvenlik kurulumunda daha uzun süre yatırım gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-160">The service might require longer time investments in endpoint and security setup.</span></span></li><li><span data-ttu-id="f5c29-161">Hizmet kendi kendine yönetilir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-161">The service is self-managed.</span></span></li><li><span data-ttu-id="f5c29-162">Hizmet kendi kendine izlenir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-162">The service is self-monitored.</span></span></li></ul> |

<span data-ttu-id="f5c29-163">Aşağıdaki resimde, harici bir CDN hizmeti içeren bir Commerce altyapısı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f5c29-163">The following illustration shows a Commerce infrastructure that includes an external CDN service.</span></span>

![Harici CDN hizmeti içeren Commerce altyapısı](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a><span data-ttu-id="f5c29-165">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f5c29-165">Additional resources</span></span>

[<span data-ttu-id="f5c29-166">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="f5c29-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
