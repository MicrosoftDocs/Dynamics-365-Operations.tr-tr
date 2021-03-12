---
title: Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme
description: Bu konu, Microsoft Dynamics 365 Commerce sitenizin bir veya daha fazla çevrimiçi mağazaya nasıl bağlanacağını açıklamaktadır.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc93441bd09deccdb8c7ecf955c0ec5177c0b31e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980035"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="3849d-103">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3849d-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3849d-104">Bu konu, Microsoft Dynamics 365 Commerce sitenizin bir veya daha fazla çevrimiçi mağazaya nasıl bağlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="3849d-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="3849d-105">Microsoft Dynamics Lifecycle Services (LCS) portalını kullanarak e-ticaret sağlandıktan sonra, ilk Dynamics 365 Commerce e-ticaret Web sitenizi hazırlıyoruz.</span><span class="sxs-lookup"><span data-stu-id="3849d-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="3849d-106">İlk site oluşturma işleminin bir parçası olarak, siteyi önceden oluşturulmuş bir çevrimiçi mağazadan ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3849d-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="3849d-107">Bu adım, siteyi çevrimiçi bir kanala bağlar ve sitenin gezinti hiyerarşisini, ürünlerini, kategorilerini, fiyatlarını, Sevkiyat seçeneklerini ve çevrimiçi mağazada tanımladığınız her şeyi göstermesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="3849d-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="3849d-108">Yeni bir site oluşturmak ve bir çevrimiçi mağazayı bununla ilişkilendirmek için, LCS'de, site yazma ortamı bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="3849d-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="3849d-109">Sonra, site geliştirme ortamının sayfasında **Yeni site**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3849d-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="3849d-110">**Yeni site** iletişim kutusunda, siteniz hakkında bazı temel bilgileri sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3849d-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="3849d-111">Sağlamanız gereken bilgilerin tam açıklaması için, [yeni bir e-ticaret sitesi oluşturma](create-ecommerce-site.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="3849d-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="3849d-112">Siteniz oluşturulduktan sonra, **ürünler** sekmesini seçerek çevrimiçi deponuzla ilişkili olduğunu doğrulayabilirsiniz. Çevrimiçi mağazaya tahsis edilen ürün sınıflamayı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="3849d-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="3849d-113">Ürünlere göre ürüne erişmek için sayfanın sol üst tarafındaki açılan alanı da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3849d-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3849d-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3849d-114">Additional resources</span></span>

[<span data-ttu-id="3849d-115">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3849d-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3849d-116">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="3849d-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3849d-117">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3849d-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="3849d-118">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="3849d-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3849d-119">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="3849d-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="3849d-120">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="3849d-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="3849d-121">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="3849d-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3849d-122">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3849d-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="3849d-123">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="3849d-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3849d-124">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3849d-124">Enable location-based store detection</span></span>](enable-store-detection.md)
