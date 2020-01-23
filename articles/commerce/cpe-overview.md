---
title: Ticaret önizleme ortamına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce önizleme ortamı genel görünümünü vermektedir.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906082"
---
# <a name="commerce-preview-environment-overview"></a><span data-ttu-id="51895-103">Ticaret önizleme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="51895-103">Commerce preview environment overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="51895-104">Bu konu, Microsoft Dynamics 365 Commerce önizleme ortamı genel görünümünü vermektedir.</span><span class="sxs-lookup"><span data-stu-id="51895-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="51895-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="51895-105">Overview</span></span>

<span data-ttu-id="51895-106">Commerce önizleme ortamı, müşterilerin genel kullanıma açık sürümünden önce Commerce ürününü denemesini sağlayan isteğe bağlı bir uçtan uca Dynamics 365 Commerce önizleme ortamıdır.</span><span class="sxs-lookup"><span data-stu-id="51895-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="51895-107">Özellikleri veya işlevleri etkilemeyen bazı küçük sınırlamalardan dolayı, Commerce önizleme ortamı eksiksiz bir ticaret deneyimi sağlar ve müşteriler ve uygulama ortakları tarafından ürünü değerlendirmek, geribildirim sağlamak ve sığdırma/boşluk analizi yapmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="51895-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="51895-108">Commerce önizleme ortamının sınırlamaları</span><span class="sxs-lookup"><span data-stu-id="51895-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="51895-109">Commerce önizleme ortamı tam ticari özellik ve işlevsellik kümesini sağlasa da, küçük bazı sınırlamalar vardır:</span><span class="sxs-lookup"><span data-stu-id="51895-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="51895-110">Commerce önizleme ortamının kendisinin hiç coğrafi sınırlamaları olmamasına rağmen, Retail Cloud Scale Unit (RCSU) ve e-ticaret uygulamaları gibi ortam bileşenleri yalnızca Amerika Birleşik Devletleri sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="51895-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="51895-111">Commerce önizleme ortamının kullanımında, e-ticaret sağlama tarihinden itibaren 30 günlük zaman sınırlaması vardır.</span><span class="sxs-lookup"><span data-stu-id="51895-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="51895-112">Commerce önizleme ortamı, yalnızca bir ortamdaki tüm bileşenlerin tek bir sanal makinede (VM) dağıtıldığı gösteri topolojisini kullanan bir ortamda başarıyla dağıtılabilir ve başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="51895-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="51895-113">Bu OneBox VM topolojisinin ana sınırlaması, önizleme ortamının destekleyebileceği eşzamanlı kullanıcı sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="51895-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="51895-114">Ticari önizleme ortamı yalnızca, ticaret ürününün genel kullanılabilirliği (GA) kadar değerlendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="51895-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="51895-115">Yeni tanıtım ortamları GA'dan sonra kullanılabilecektir.</span><span class="sxs-lookup"><span data-stu-id="51895-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="51895-116">Başlayın</span><span class="sxs-lookup"><span data-stu-id="51895-116">Get started</span></span>

<span data-ttu-id="51895-117">Commerce önizleme ortamını sağlamak için bkz. [Commerce önizleme ortamı sağlama](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="51895-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51895-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="51895-118">Additional resources</span></span>

[<span data-ttu-id="51895-119">Ticaret önizleme ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="51895-119">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="51895-120">Ticaret önizleme ortamı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="51895-120">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="51895-121">Bir Commerce Preview ortamı için isteğe bağlı özellikleri konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="51895-121">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="51895-122">Ticaret önizleme ortamı SSS</span><span class="sxs-lookup"><span data-stu-id="51895-122">Commerce preview environment FAQ</span></span>](cpe-faq.md)
