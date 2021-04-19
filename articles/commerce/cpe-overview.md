---
title: Dynamics 365 Commerce değerlendirme ortamına genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı genel görünümünü vermektedir.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bdd634a04b6bbcf50d04cae8d670367268e57f1e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795895"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="a5349-103">Dynamics 365 Commerce değerlendirme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="a5349-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a5349-104">Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı genel görünümünü vermektedir.</span><span class="sxs-lookup"><span data-stu-id="a5349-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="a5349-105">Commerce değerlendirme ortamları genel olarak kullanıma sunulmamıştır ve iş ortakları ile müşterilere istek üzerine sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a5349-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="a5349-106">Daha fazla bilgi için Microsoft iş ortağı ilgili kişisine ulaşın.</span><span class="sxs-lookup"><span data-stu-id="a5349-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="a5349-107">Commerce değerlendirme ortamı, iş ortaklarının ve potansiyel müşterilerin Commerce ürününü denemesini sağlayan isteğe bağlı bir uçtan uca Dynamics 365 Commerce değerlendirme ortamıdır.</span><span class="sxs-lookup"><span data-stu-id="a5349-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="a5349-108">Değerlendirme ortamları, gerekli sağlama sonrası adımları azaltmak amacıyla kısmi olarak önceden yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="a5349-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="a5349-109">Özellikleri veya işlevleri etkilemeyen bazı küçük sınırlamalara karşın, Commerce değerlendirme ortamı eksiksiz bir ticaret deneyimi sağlar ve müşteriler ve uygulama ortakları tarafından ürünü değerlendirmek, geribildirim sağlamak ve uygunluk/boşluk analizi yapmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a5349-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="a5349-110">Commerce değerlendirme ortamının sınırlamaları</span><span class="sxs-lookup"><span data-stu-id="a5349-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="a5349-111">Commerce değerlendirme ortamı tam Commerce özellik ve işlevsellik kümesini sağlasa da, küçük bazı sınırlamalar vardır:</span><span class="sxs-lookup"><span data-stu-id="a5349-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="a5349-112">Commerce değerlendirme ortamının hiç coğrafi sınırlaması olmamasına karşın, Retail Cloud Scale Unit (RCSU) ve e-Ticaret uygulamaları gibi ortam bileşenleri yalnızca Amerika Birleşik Devletleri'nde sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a5349-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="a5349-113">Commerce değerlendirme ortamının kullanımında, e-Ticaret sağlama tarihinden itibaren 30 günlük zaman sınırlaması vardır.</span><span class="sxs-lookup"><span data-stu-id="a5349-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="a5349-114">Commerce değerlendirme ortamı, yalnızca bir ortamdaki tüm bileşenlerin bulutta barındırılan tek bir sanal makinede (VM) dağıtıldığı gösteri topolojisini kullanan bir ortamda başarıyla dağıtılabilir ve başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="a5349-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="a5349-115">Bu topolojinin ana sınırlaması, ortamın destekleyebileceği eşzamanlı kullanıcı sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="a5349-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="a5349-116">Başlayın</span><span class="sxs-lookup"><span data-stu-id="a5349-116">Get started</span></span>

<span data-ttu-id="a5349-117">Commerce değerlendirme ortamını sağlamak için bkz. [Commerce değerlendirme ortamı sağlama](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="a5349-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5349-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a5349-118">Additional resources</span></span>

[<span data-ttu-id="a5349-119">Dynamics 365 Commerce değerlendirme ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="a5349-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="a5349-120">Dynamics 365 Commerce değerlendirme ortamı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a5349-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="a5349-121">Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a5349-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="a5349-122">Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a5349-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="a5349-123">Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="a5349-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
