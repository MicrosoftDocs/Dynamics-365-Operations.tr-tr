---
title: E-ticaret sitesi oluşturma
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cf084f90d203d84c91ddf7c0d963780b895ef23d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963047"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="ea4fd-103">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea4fd-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea4fd-104">Bu konu, Dynamics 365 Commerce site oluşturucusunda yeni bir e-ticaret sitesi oluşturmak için gereken adımları ve bilgileri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="ea4fd-105">Dynamics 365 Commerce yeteneklerine lisans verirken, site oluşturucu, kendi siteniz için temel olarak kullanabileceğiniz bir başlatıcı siteyle hazırlanacak.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="ea4fd-106">Ancak, baştan başlatmak veya ikinci bir site oluşturmak istiyorsanız, site geliştirme ortamında yeni bir site oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="ea4fd-107">Sitenizi ayarlama</span><span class="sxs-lookup"><span data-stu-id="ea4fd-107">Set up your site</span></span>

<span data-ttu-id="ea4fd-108">Sitenizi kurmak için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="ea4fd-109">Site oluşturucu ortamını açın.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-109">Open the site builder environment.</span></span> <span data-ttu-id="ea4fd-110">Microsoft Lifecycle Services'teki (LCS) site oluşturucuya bir bağlantıyı Commerce'in ortam özellikleri sayfasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="ea4fd-111">Site geliştirme ortamının giriş sayfasında **Yeni site**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="ea4fd-112">**Yeni site** iletişim kutusuna, aşağıdaki bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="ea4fd-113">Alan</span><span class="sxs-lookup"><span data-stu-id="ea4fd-113">Field</span></span>                               | <span data-ttu-id="ea4fd-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea4fd-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="ea4fd-115">Site adı</span><span class="sxs-lookup"><span data-stu-id="ea4fd-115">Site name</span></span>                           | <span data-ttu-id="ea4fd-116">Site geliştirme ortamında siteniz için kullanılacak görünen adı girin.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="ea4fd-117">Bu ad yalnızca geliştirme ortamında görünür ve müşteriler tarafından gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="ea4fd-118">Site yöneticisinin güvenlik grubu</span><span class="sxs-lookup"><span data-stu-id="ea4fd-118">Site administrator's security group</span></span> | <span data-ttu-id="ea4fd-119">Bu sitede site Yöneticisi rolüne sahip kullanıcıları yöneten Microsoft Azure Active Directory (Azure AD) güvenlik grubunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="ea4fd-120">Varsayılan kanal (faaliyet birimi numarası)</span><span class="sxs-lookup"><span data-stu-id="ea4fd-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="ea4fd-121">Bu sitenin Web mağazası olarak hizmet verdiği çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="ea4fd-122">E-ticaret sitenizin çoklu çevrimiçi mağazaları desteklemesini istiyorsanız, site yüklendikten sonra depoları **site ayarlarında** siteyle ilişkilendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="ea4fd-123">Varsayılan dil</span><span class="sxs-lookup"><span data-stu-id="ea4fd-123">Default language</span></span>                            | <span data-ttu-id="ea4fd-124">Bu çevrimiçi mağaza ve pazar için varsayılan dili belirtin.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="ea4fd-125">Çevrimiçi bir mağaza birden çok dili destekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-125">An online store can support multiple languages.</span></span> <span data-ttu-id="ea4fd-126">Bu çevrimiçi mağaza veya başka bir çevrimiçi mağaza için birden fazla dili desteklemek istiyorsanız, site yüklendikten sonra bu desteği **Site Ayarları**'nda yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="ea4fd-127">Etki Alanı</span><span class="sxs-lookup"><span data-stu-id="ea4fd-127">Domain</span></span>                              | <span data-ttu-id="ea4fd-128">Bu çevrimiçi mağaza için etki alanı olarak hizmet verdiği etki alanı adını seçin.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="ea4fd-129">LCS'de herhangi bir etki alanı konfigüre etmediyseniz, bu alanı boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="ea4fd-130">Etki alanınız LCS'de yapılandırıldıktan sonra, **Site ayarlarındaki** çevrimiçi deponuza eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="ea4fd-131">Yol</span><span class="sxs-lookup"><span data-stu-id="ea4fd-131">Path</span></span>                              | <span data-ttu-id="ea4fd-132">Siteniz belirli bir etki alanı adı için birden fazla dili destekliyorsa, bu etki alanı ve dil birleşimi için benzersiz bir site URL 'SI oluşturmak üzere yol alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="ea4fd-133">**Varsayılan dil** alanında belirttiğiniz dil bu etki alanı için desteklerinizin tek dili ise veya sitenizi ek dillere yerelleştirdikten sonra varsayılan dil olmaya devam edecek ise, bu alanı boş bırakmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="ea4fd-134">Siteniz oluşturulduktan sonra, **ürünler** sekmesini seçerek çevrimiçi deponuzla ilişkili olduğunu doğrulayabilirsiniz. Çevrimiçi mağazaya tahsis edilen ürün sınıflamayı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="ea4fd-135">Kategoriye göre ilgili ürüne erişmek için sayfanın sol üst tarafındaki açılan menüyü da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea4fd-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea4fd-136">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ea4fd-136">Additional resources</span></span>

[<span data-ttu-id="ea4fd-137">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ea4fd-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ea4fd-138">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="ea4fd-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ea4fd-139">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="ea4fd-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ea4fd-140">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="ea4fd-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="ea4fd-141">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="ea4fd-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="ea4fd-142">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="ea4fd-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="ea4fd-143">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="ea4fd-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="ea4fd-144">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ea4fd-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="ea4fd-145">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="ea4fd-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ea4fd-146">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ea4fd-146">Enable location-based store detection</span></span>](enable-store-detection.md)
