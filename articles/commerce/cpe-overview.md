---
title: Dynamics 365 Commerce değerlendirme ortamına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı genel görünümünü vermektedir.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416320"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="2eead-103">Dynamics 365 Commerce değerlendirme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="2eead-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2eead-104">Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı genel görünümünü vermektedir.</span><span class="sxs-lookup"><span data-stu-id="2eead-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="2eead-105">Commerce değerlendirme ortamları genel olarak kullanıma sunulmamıştır ve iş ortakları ile müşterilere istek üzerine sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2eead-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="2eead-106">Daha fazla bilgi için Microsoft iş ortağı ilgili kişisine ulaşın.</span><span class="sxs-lookup"><span data-stu-id="2eead-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="2eead-107">Özet</span><span class="sxs-lookup"><span data-stu-id="2eead-107">Overview</span></span>

<span data-ttu-id="2eead-108">Commerce değerlendirme ortamı, iş ortaklarının ve potansiyel müşterilerin Commerce ürününü denemesini sağlayan isteğe bağlı bir uçtan uca Dynamics 365 Commerce değerlendirme ortamıdır.</span><span class="sxs-lookup"><span data-stu-id="2eead-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="2eead-109">Değerlendirme ortamları, gerekli sağlama sonrası adımları azaltmak amacıyla kısmi olarak önceden yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="2eead-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="2eead-110">Özellikleri veya işlevleri etkilemeyen bazı küçük sınırlamalara karşın, Commerce değerlendirme ortamı eksiksiz bir ticaret deneyimi sağlar ve müşteriler ve uygulama ortakları tarafından ürünü değerlendirmek, geribildirim sağlamak ve uygunluk/boşluk analizi yapmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2eead-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="2eead-111">Commerce değerlendirme ortamının sınırlamaları</span><span class="sxs-lookup"><span data-stu-id="2eead-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="2eead-112">Commerce değerlendirme ortamı tam Commerce özellik ve işlevsellik kümesini sağlasa da, küçük bazı sınırlamalar vardır:</span><span class="sxs-lookup"><span data-stu-id="2eead-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="2eead-113">Commerce değerlendirme ortamının hiç coğrafi sınırlaması olmamasına karşın, Retail Cloud Scale Unit (RCSU) ve e-Ticaret uygulamaları gibi ortam bileşenleri yalnızca Amerika Birleşik Devletleri'nde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="2eead-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="2eead-114">Commerce değerlendirme ortamının kullanımında, e-Ticaret sağlama tarihinden itibaren 30 günlük zaman sınırlaması vardır.</span><span class="sxs-lookup"><span data-stu-id="2eead-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="2eead-115">Commerce değerlendirme ortamı, yalnızca bir ortamdaki tüm bileşenlerin bulutta barındırılan tek bir sanal makinede (VM) dağıtıldığı gösteri topolojisini kullanan bir ortamda başarıyla dağıtılabilir ve başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="2eead-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="2eead-116">Bu topolojinin ana sınırlaması, ortamın destekleyebileceği eşzamanlı kullanıcı sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="2eead-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="2eead-117">Başlayın</span><span class="sxs-lookup"><span data-stu-id="2eead-117">Get started</span></span>

<span data-ttu-id="2eead-118">Commerce değerlendirme ortamını sağlamak için bkz. [Commerce değerlendirme ortamı sağlama](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="2eead-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2eead-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2eead-119">Additional resources</span></span>

[<span data-ttu-id="2eead-120">Dynamics 365 Commerce değerlendirme ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="2eead-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="2eead-121">Dynamics 365 Commerce değerlendirme ortamı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2eead-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="2eead-122">Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2eead-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="2eead-123">Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2eead-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="2eead-124">Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="2eead-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
