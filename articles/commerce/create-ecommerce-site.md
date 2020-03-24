---
title: e-Ticaret sitesi oluşturma
description: Bu konu, Dynamics 365 Commerce site oluşturucusunda yeni bir e-ticaret sitesi oluşturmak için gereken adımları ve bilgileri açıklamaktadır.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
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
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096786"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="efb79-103">e-Ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="efb79-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="efb79-104">Bu konu, Dynamics 365 Commerce site oluşturucusunda yeni bir e-ticaret sitesi oluşturmak için gereken adımları ve bilgileri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="efb79-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="efb79-105">E-ticaret sitenizi geliştirmeye başlamadan önce, site oluşturucuda yeni bir site oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="efb79-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="efb79-106">E-ticaret sitenizi geliştirmeye başlamak için, önce site geliştirme ortamında yeni bir site oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="efb79-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="efb79-107">Yeni bir site oluşturabilmeniz için, Commerce'te en az bir çevrimiçi mağazanın oluşturulması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="efb79-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="efb79-108">Sitenizi ayarlama</span><span class="sxs-lookup"><span data-stu-id="efb79-108">Set up your site</span></span>

<span data-ttu-id="efb79-109">Sitenizi kurmak için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="efb79-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="efb79-110">Site oluşturucu ortamını açın.</span><span class="sxs-lookup"><span data-stu-id="efb79-110">Open the site builder environment.</span></span> <span data-ttu-id="efb79-111">Microsoft Lifecycle Services'teki (LCS) site oluşturucuya bir bağlantıyı Commerce'in ortam özellikleri sayfasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="efb79-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="efb79-112">Site geliştirme ortamının giriş sayfasında **Yeni site**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="efb79-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="efb79-113">**Yeni site** iletişim kutusuna, aşağıdaki bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="efb79-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="efb79-114">Alan</span><span class="sxs-lookup"><span data-stu-id="efb79-114">Field</span></span>                               | <span data-ttu-id="efb79-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="efb79-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="efb79-116">Site adı</span><span class="sxs-lookup"><span data-stu-id="efb79-116">Site name</span></span>                           | <span data-ttu-id="efb79-117">Site geliştirme ortamında siteniz için kullanılacak görünen adı girin.</span><span class="sxs-lookup"><span data-stu-id="efb79-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="efb79-118">Bu ad yalnızca geliştirme ortamında görünür ve müşteriler tarafından gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="efb79-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="efb79-119">Site yöneticisinin güvenlik grubu</span><span class="sxs-lookup"><span data-stu-id="efb79-119">Site administrator's security group</span></span> | <span data-ttu-id="efb79-120">Bu sitede site Yöneticisi rolüne sahip kullanıcıları yöneten Microsoft Azure Active Directory (Azure AD) güvenlik grubunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="efb79-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="efb79-121">Varsayılan kanal (faaliyet birimi numarası)</span><span class="sxs-lookup"><span data-stu-id="efb79-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="efb79-122">Bu sitenin Web mağazası olarak hizmet verdiği çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="efb79-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="efb79-123">E-ticaret sitenizin çoklu çevrimiçi mağazaları desteklemesini istiyorsanız, site yüklendikten sonra depoları **site ayarlarında** siteyle ilişkilendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="efb79-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="efb79-124">Varsayılan dil</span><span class="sxs-lookup"><span data-stu-id="efb79-124">Default language</span></span>                            | <span data-ttu-id="efb79-125">Bu çevrimiçi mağaza ve pazar için varsayılan dili belirtin.</span><span class="sxs-lookup"><span data-stu-id="efb79-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="efb79-126">Çevrimiçi bir mağaza birden çok dili destekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="efb79-126">An online store can support multiple languages.</span></span> <span data-ttu-id="efb79-127">Bu çevrimiçi mağaza veya başka bir çevrimiçi mağaza için birden fazla dili desteklemek istiyorsanız, site yüklendikten sonra bu desteği **Site Ayarları**'nda yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="efb79-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="efb79-128">Etki Alanı</span><span class="sxs-lookup"><span data-stu-id="efb79-128">Domain</span></span>                              | <span data-ttu-id="efb79-129">Bu çevrimiçi mağaza için etki alanı olarak hizmet verdiği etki alanı adını seçin.</span><span class="sxs-lookup"><span data-stu-id="efb79-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="efb79-130">LCS'de herhangi bir etki alanı konfigüre etmediyseniz, bu alanı boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="efb79-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="efb79-131">Etki alanınız LCS'de yapılandırıldıktan sonra, **Site ayarlarındaki** çevrimiçi deponuza eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="efb79-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="efb79-132">Yol</span><span class="sxs-lookup"><span data-stu-id="efb79-132">Path</span></span>                              | <span data-ttu-id="efb79-133">Siteniz belirli bir etki alanı adı için birden fazla dili destekliyorsa, bu etki alanı ve dil birleşimi için benzersiz bir site URL 'SI oluşturmak üzere yol alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="efb79-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="efb79-134">**Varsayılan dil** alanında belirttiğiniz dil bu etki alanı için desteklerinizin tek dili ise veya sitenizi ek dillere yerelleştirdikten sonra varsayılan dil olmaya devam edecek ise, bu alanı boş bırakmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="efb79-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="efb79-135">Siteniz oluşturulduktan sonra, **ürünler** sekmesini seçerek çevrimiçi deponuzla ilişkili olduğunu doğrulayabilirsiniz. Çevrimiçi mağazaya tahsis edilen ürün sınıflamayı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="efb79-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="efb79-136">Kategoriye göre ilgili ürüne erişmek için sayfanın sol üst tarafındaki açılan menüyü da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="efb79-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="efb79-137">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="efb79-137">Additional resources</span></span>

[<span data-ttu-id="efb79-138">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="efb79-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="efb79-139">Yeni e-Ticaret sitesini dağıtma</span><span class="sxs-lookup"><span data-stu-id="efb79-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="efb79-140">Çevrimiçi mağaza kanalı ayarlama</span><span class="sxs-lookup"><span data-stu-id="efb79-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="efb79-141">Çevrimiçi siteyi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="efb79-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="efb79-142">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="efb79-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="efb79-143">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="efb79-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="efb79-144">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="efb79-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="efb79-145">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="efb79-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="efb79-146">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="efb79-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="efb79-147">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="efb79-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="efb79-148">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="efb79-148">Enable location-based store detection</span></span>](enable-store-detection.md)
