---
title: Etki alanı adınızı yapılandırma
description: Bu konu, Microsoft Dynamics 365 e-ticaret sitesi için etki alanı adının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8b7bc322b1a42190d5eec99f89a34025c34ba09f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220498"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="6ed9b-103">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6ed9b-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6ed9b-104">Bu konu, Microsoft Dynamics 365 e-ticaret sitesi için etki alanı adının nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="6ed9b-105">E-ticaret başlatma sırasında etki alanları ekleme</span><span class="sxs-lookup"><span data-stu-id="6ed9b-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="6ed9b-106">Etki alanlarını Dynamics 365 Commerce e-ticaret ortamınızla ilişkilendirmek için, [yeni e-ticaret kiracısı dağıtma](deploy-ecommerce-site.md) konusunda açıklandığı gibi e-ticaret başlatın.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="6ed9b-107">Başlatma sırasında, e-ticaret ortamınızı sağlamak için kullanılacak bilgileri vermeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="6ed9b-108">**Desteklenen ana bilgisayar adları** alanında, bu ortamda kullanmayı planladığınız tüm etki alanlarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="6ed9b-109">Birden çok etki alanı noktalı virgül ile ayrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="6ed9b-110">Bu şekilde, etki alanları gerekli tüm e-ticaret bileşenlerinde yapılandırılır ve içerik teslim ağından (CDN) veya Web sunucusundan gelen trafiği değiştirdiğinizde ve bunu e-ticaret ön uçlarına işaret ettiğinizde kullanılmaya hazır hale gelir.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="6ed9b-111">E-ticaret başlatmadan sonra etki alanları ekleme</span><span class="sxs-lookup"><span data-stu-id="6ed9b-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="6ed9b-112">E-ticaret başlatmasının ardından yeni etki alanlarını e-ticaret ortamınızla ilişkilendirmek için, bir servis isteği göndermeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6ed9b-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ed9b-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6ed9b-113">Additional resources</span></span>

[<span data-ttu-id="6ed9b-114">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="6ed9b-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6ed9b-115">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6ed9b-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6ed9b-116">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="6ed9b-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6ed9b-117">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="6ed9b-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6ed9b-118">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="6ed9b-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="6ed9b-119">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="6ed9b-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="6ed9b-120">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="6ed9b-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6ed9b-121">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6ed9b-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6ed9b-122">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="6ed9b-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6ed9b-123">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6ed9b-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]