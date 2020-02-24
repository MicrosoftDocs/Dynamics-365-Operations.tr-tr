---
title: Derecelendirme ve incelemelere genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'ta bulunan derecelendirmeleri ve incelemelerini kapsamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 49587bb497288fc6f3ce77f04a378fc67056ecf2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002878"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="5ac2f-103">Derecelendirme ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="5ac2f-103">Ratings and reviews overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5ac2f-104">Bu konu, Microsoft Dynamics 365 Commerce'ta bulunan derecelendirmeleri ve incelemelerini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5ac2f-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="5ac2f-105">Overview</span></span>

<span data-ttu-id="5ac2f-106">Derecelendirmeler ve incelemeler, diğer müşterilerin bir ürünü nasıl değerlendirdiklerini öğrenmek isteyen e-ticaret müşterileri için çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="5ac2f-107">Ayrıca, tüketicilerin satın alma kararları verbilmesine yardımcı olabilirler.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="5ac2f-108">Dynamics 365 Commerce'De, derecelendirmeler ve İncelemeler çözümünde perakendecilerin ürün incelemelerini ve müşterilerden gelen derecelendirmeleri yakalayabilmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="5ac2f-109">Perakendeciler, ortalama derecelendirmeleri gösterebilir ve e-ticaret Web siteleri boyunca bilgileri gözden geçirebilir.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="5ac2f-110">Ortalama derecelendirme bilgileri, satış noktasında (POS) ve çağrı merkezi kanallarında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="5ac2f-111">Bu nedenle, satış temsilcileri kullanıcıların kararlar vermelerini sağlamak için bunu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="5ac2f-112">Derecelendirmeler ve incelemeler ayrıca, perakendecinin bir ürünün kalitesini artırmak için kullanabileceği bir geri bildirim mekanizması olarak hizmet verebilir ve bu nedenle satışları artırabilir.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="5ac2f-113">Dynamics 365 Commerce'deki derecelendirmeler ve İncelemeler işlevselliği bir çok yönlü kanal çözümüdür ve platformun bir parçası olarak doğal olarak mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="5ac2f-114">Derecelendirmeler ve İncelemeler çözümü yüksek ölçeklenebilirliği ve güvenilirliği sağlayan Microsoft Azure en üst sürümü geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="5ac2f-115">Aşağıdaki şekil, derecelendirmelerin ve İncelemeler çözümünün Dynamics 365 Commerce'te nasıl çalıştığı göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![Dynamics 365 for Commerce'te Derecelendirmeler ve incelemeler](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="5ac2f-117">Dynamics 365 Commerce'teki derecelendirmeler ve İncelemeler çözümü, 40 dilde argo sözcüklerin otomatik olarak yumuşatmasını sağlamak için Azure Cognitive Services'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="5ac2f-118">İnsan onayı gerekli olmadığından, denetleme maliyetleri azalır.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="5ac2f-119">Sistem Ayrıca, müşteri kaygıları, görüşleri ve açılan isteklerin yanıtlanması ve kullanıcılardan gelen veri isteklerini adreslemek için kullanılabilen aracı araçları da sunar.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="5ac2f-120">Derecelendirmeler ve İncelemeler çözümü, ürün listelerindeki, arama sonuçlarında, ürün ayrıntıları sayfasındaki ve diğer yerlerde değerlendirme özetlerini gösteren pencere öğeleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="5ac2f-121">Pencere öğeleri tam gözden geçirme listelerini gösterir ve ayrıca sıralama ve süzme seçenekleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="5ac2f-122">Derecelendirmeler ve İncelemeler çözümü Ayrıca derecelendirmelere ve incelemelere Öngörüler sağlamak üzere bir dizi ölçüm içeren bir iş zekası (BI) şablonu sağlar.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="5ac2f-123">Derecelendirme ve gözden geçirme verileri, daha fazla analiz için dışa aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ac2f-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ac2f-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5ac2f-124">Additional resources</span></span>

[<span data-ttu-id="5ac2f-125">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="5ac2f-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="5ac2f-126">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="5ac2f-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="5ac2f-127">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5ac2f-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="5ac2f-128">Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="5ac2f-128">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
