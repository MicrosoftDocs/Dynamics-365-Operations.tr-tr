---
title: Etki alanı adınızı yapılandırma
description: Bu konu, Microsoft Dynamics 365 e-ticaret sitesi için etki alanı adının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770470"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="8097b-103">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8097b-103">Configure your domain name</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8097b-104">Bu konu, Microsoft Dynamics 365 e-ticaret sitesi için etki alanı adının nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="8097b-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="8097b-105">E-ticaret başlatma sırasında etki alanları ekleme</span><span class="sxs-lookup"><span data-stu-id="8097b-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="8097b-106">Etki alanlarını e-ticaret ortamınızla ilişkilendirmek için, [yeni e-ticaret sitesini dağıtma](deploy-ecommerce-site.md) konusunda açıklandığı gibi e-ticaret başlatın.</span><span class="sxs-lookup"><span data-stu-id="8097b-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="8097b-107">Başlatma sırasında, e-ticaret ortamınızı sağlamak için kullanılacak bilgileri vermeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="8097b-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="8097b-108">**Desteklenen ana bilgisayar adları** alanında, bu ortamda kullanmayı planladığınız tüm etki alanlarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8097b-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="8097b-109">Birden çok etki alanı noktalı virgül ile ayrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8097b-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="8097b-110">Bu şekilde, etki alanları gerekli tüm e-ticaret bileşenlerinde yapılandırılır ve içerik teslim ağından (CDN) veya Web sunucusundan gelen trafiği değiştirdiğinizde ve bunu e-ticaret ön uçlarına işaret ettiğinizde kullanılmaya hazır hale gelir.</span><span class="sxs-lookup"><span data-stu-id="8097b-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="8097b-111">E-ticaret başlatmadan sonra etki alanları ekleme</span><span class="sxs-lookup"><span data-stu-id="8097b-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="8097b-112">E-ticaret başlatmasının ardından yeni etki alanlarını e-ticaret ortamınızla ilişkilendirmek için, bir servis isteği göndermeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8097b-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8097b-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8097b-113">Additional resources</span></span>

[<span data-ttu-id="8097b-114">Çevrimiçi mağazaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="8097b-114">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="8097b-115">e-Ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8097b-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="8097b-116">Yeni e-Ticaret sitesini dağıtma</span><span class="sxs-lookup"><span data-stu-id="8097b-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="8097b-117">Çevrimiçi siteyi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="8097b-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8097b-118">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="8097b-118">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="8097b-119">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="8097b-119">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="8097b-120">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="8097b-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
