---
title: e-Ticaret sitesi oluşturma
description: Bu konu, Dynamics 365 Commerce site oluşturucusunda yeni bir e-ticaret sitesi oluşturmak için gereken adımları ve bilgileri açıklamaktadır.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ea3517a4f2b84db8a87a97d2f644bb4436f8693f
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533448"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="92f63-103">e-Ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="92f63-103">Create an e-Commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92f63-104">Bu konu, Dynamics 365 Commerce site oluşturucusunda yeni bir e-ticaret sitesi oluşturmak için gereken adımları ve bilgileri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="92f63-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="92f63-105">E-ticaret yeteneklerine lisans verirken, site oluşturucu, kendi siteniz için temel olarak kullanabileceğiniz bir başlatıcı siteyle hazırlanacak.</span><span class="sxs-lookup"><span data-stu-id="92f63-105">When you license the e-Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="92f63-106">Ancak, baştan başlatmak veya ikinci bir site oluşturmak istiyorsanız, site geliştirme ortamında yeni bir site oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="92f63-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="92f63-107">Sitenizi ayarlama</span><span class="sxs-lookup"><span data-stu-id="92f63-107">Set up your site</span></span>

<span data-ttu-id="92f63-108">Sitenizi kurmak için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="92f63-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="92f63-109">Site oluşturucu ortamını açın.</span><span class="sxs-lookup"><span data-stu-id="92f63-109">Open the site builder environment.</span></span> <span data-ttu-id="92f63-110">Microsoft Lifecycle Services'teki (LCS) site oluşturucuya bir bağlantıyı Commerce'in ortam özellikleri sayfasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92f63-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="92f63-111">Site geliştirme ortamının giriş sayfasında **Yeni site**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="92f63-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="92f63-112">**Yeni site** iletişim kutusuna, aşağıdaki bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="92f63-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="92f63-113">Alan</span><span class="sxs-lookup"><span data-stu-id="92f63-113">Field</span></span>                               | <span data-ttu-id="92f63-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="92f63-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="92f63-115">Site adı</span><span class="sxs-lookup"><span data-stu-id="92f63-115">Site name</span></span>                           | <span data-ttu-id="92f63-116">Site geliştirme ortamında siteniz için kullanılacak görünen adı girin.</span><span class="sxs-lookup"><span data-stu-id="92f63-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="92f63-117">Bu ad yalnızca geliştirme ortamında görünür ve müşteriler tarafından gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="92f63-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="92f63-118">Site yöneticisinin güvenlik grubu</span><span class="sxs-lookup"><span data-stu-id="92f63-118">Site administrator's security group</span></span> | <span data-ttu-id="92f63-119">Bu sitede site Yöneticisi rolüne sahip kullanıcıları yöneten Microsoft Azure Active Directory (Azure AD) güvenlik grubunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="92f63-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="92f63-120">Varsayılan kanal (faaliyet birimi numarası)</span><span class="sxs-lookup"><span data-stu-id="92f63-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="92f63-121">Bu sitenin Web mağazası olarak hizmet verdiği çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="92f63-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="92f63-122">E-ticaret sitenizin çoklu çevrimiçi mağazaları desteklemesini istiyorsanız, site yüklendikten sonra depoları **site ayarlarında** siteyle ilişkilendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="92f63-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="92f63-123">Varsayılan dil</span><span class="sxs-lookup"><span data-stu-id="92f63-123">Default language</span></span>                            | <span data-ttu-id="92f63-124">Bu çevrimiçi mağaza ve pazar için varsayılan dili belirtin.</span><span class="sxs-lookup"><span data-stu-id="92f63-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="92f63-125">Çevrimiçi bir mağaza birden çok dili destekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="92f63-125">An online store can support multiple languages.</span></span> <span data-ttu-id="92f63-126">Bu çevrimiçi mağaza veya başka bir çevrimiçi mağaza için birden fazla dili desteklemek istiyorsanız, site yüklendikten sonra bu desteği **Site Ayarları**'nda yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92f63-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="92f63-127">Etki Alanı</span><span class="sxs-lookup"><span data-stu-id="92f63-127">Domain</span></span>                              | <span data-ttu-id="92f63-128">Bu çevrimiçi mağaza için etki alanı olarak hizmet verdiği etki alanı adını seçin.</span><span class="sxs-lookup"><span data-stu-id="92f63-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="92f63-129">LCS'de herhangi bir etki alanı konfigüre etmediyseniz, bu alanı boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92f63-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="92f63-130">Etki alanınız LCS'de yapılandırıldıktan sonra, **Site ayarlarındaki** çevrimiçi deponuza eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="92f63-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="92f63-131">Yol</span><span class="sxs-lookup"><span data-stu-id="92f63-131">Path</span></span>                              | <span data-ttu-id="92f63-132">Siteniz belirli bir etki alanı adı için birden fazla dili destekliyorsa, bu etki alanı ve dil birleşimi için benzersiz bir site URL 'SI oluşturmak üzere yol alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="92f63-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="92f63-133">**Varsayılan dil** alanında belirttiğiniz dil bu etki alanı için desteklerinizin tek dili ise veya sitenizi ek dillere yerelleştirdikten sonra varsayılan dil olmaya devam edecek ise, bu alanı boş bırakmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="92f63-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="92f63-134">Siteniz oluşturulduktan sonra, **ürünler** sekmesini seçerek çevrimiçi deponuzla ilişkili olduğunu doğrulayabilirsiniz. Çevrimiçi mağazaya tahsis edilen ürün sınıflamayı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="92f63-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="92f63-135">Kategoriye göre ilgili ürüne erişmek için sayfanın sol üst tarafındaki açılan menüyü da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92f63-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92f63-136">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="92f63-136">Additional resources</span></span>

[<span data-ttu-id="92f63-137">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="92f63-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="92f63-138">Yeni e-Ticaret sitesini dağıtma</span><span class="sxs-lookup"><span data-stu-id="92f63-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="92f63-139">Çevrimiçi siteyi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="92f63-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="92f63-140">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="92f63-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="92f63-141">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="92f63-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="92f63-142">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="92f63-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="92f63-143">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="92f63-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="92f63-144">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="92f63-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="92f63-145">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="92f63-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="92f63-146">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="92f63-146">Enable location-based store detection</span></span>](enable-store-detection.md)
