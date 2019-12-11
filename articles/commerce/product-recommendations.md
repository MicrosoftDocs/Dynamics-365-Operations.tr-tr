---
title: Ürün önerilerine genel bakış
description: Bu konuda ürün önerileri hakkında genel bilgiler verilmiştir. Ürün önerileri, müşterilerin istedikleri ürünleri ve hatta satın almayı amaçlamadıkları ürünleri kolayca ve hızlı bir şekilde bulmasına olanak tanır.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770059"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="f487a-104">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="f487a-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f487a-105">Microsoft Dynamics 365 Commerce, e-ticaret Web sitesi ve satış noktası (POS) aygıtında ürün önerilerini göstermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f487a-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="f487a-106">Ürün önerileri, bir müşterinin ilgilendiği öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="f487a-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="f487a-107">Öneriler, çevrimiçi ve fiziksel mağazalardaki diğer müşterilerin satın alma eğilimlerine dayanır.</span><span class="sxs-lookup"><span data-stu-id="f487a-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="f487a-108">Ürün önerileri, müşterilerin kendilerine hizmet veren bir deneyim sağlarken istedikleri ürünleri kolayca ve hızlı bir şekilde bulmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f487a-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="f487a-109">Çapraz satış ve kaplamalı ürünler, müşterilerin başlangıçta satın almayı amaçlamadıklarından daha fazla ürün bulmasına yardımcı olmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f487a-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="f487a-110">Öneriler, ürün bulma ile ilgili yardım için kullanıldığında, daha fazla dönüştürme fırsatı oluşturabilir, satış gelirini artırabilir ve hatta müşteri memnuniyetini ve korunmasını artırmaya yardımcı olabilirler.</span><span class="sxs-lookup"><span data-stu-id="f487a-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="f487a-111">Ticari olarak, Ürün önerilerinde büyük ölçekli Microsoft önerileri makine öğrenme teknolojileriyle desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="f487a-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="f487a-112">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="f487a-112">Scenarios</span></span>

<span data-ttu-id="f487a-113">Ürün önerileri aşağıdaki senaryoları için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f487a-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="f487a-114">**E-ticaret 'da gözatma veya iniş sayfası için herhangi bir depolama sayfasında:** Müşteriler veya mağaza işbirlikçileri bir mağaza sayfasını ziyaret ederken, öneri altyapısı **yeni**, **en iyi satış** ve **trend** listelerinde ürünler önerebilir.</span><span class="sxs-lookup"><span data-stu-id="f487a-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="f487a-115">**Ürün Ayrıntıları sayfasında:** müşteriler veya mağaza işbirlikçileri bir **ürün ayrıntıları** sayfasını ziyaret ederken, öneri altyapısı da büyük olasılıkla satın alınacak ek maddeleri önerir.</span><span class="sxs-lookup"><span data-stu-id="f487a-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="f487a-116">Bu öğeler, **kişiler bunları da sevdi** listesinde görünür.</span><span class="sxs-lookup"><span data-stu-id="f487a-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="f487a-117">**Hareket sayfasında veya kullanıma al sayfasında:** öneri altyapısı maddeleri sepetteki tüm madde listesine göre önerir.</span><span class="sxs-lookup"><span data-stu-id="f487a-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="f487a-118">Bu maddeler **sık kullanılan bir arada** bulunan listesinde görünür.</span><span class="sxs-lookup"><span data-stu-id="f487a-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="f487a-119">Öneri servisi</span><span class="sxs-lookup"><span data-stu-id="f487a-119">Recommendation service</span></span>

<span data-ttu-id="f487a-120">Ürün önerileri aşağıdaki şekilde öneriler makine öğrenme teknolojilerini kullanır:</span><span class="sxs-lookup"><span data-stu-id="f487a-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="f487a-121">Öneri servisinin tarafından istenen biçimdeki veriler Commerce işlem veritabanından çıkarılması ve Varlık deposuna göndermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f487a-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="f487a-122">Öneri Servisi, verileri **Bunları da sevdi**, **sık birlikte satın alınan**, **yeni**, **en iyi satış**ve **trend** listeleri gibi kişiler için öneri modelleri eğitmek üzere kullanır.</span><span class="sxs-lookup"><span data-stu-id="f487a-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f487a-123">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f487a-123">Additional resources</span></span>

[<span data-ttu-id="f487a-124">Ürün önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f487a-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="f487a-125">Seçkin ürün önerisi listeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="f487a-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="f487a-126">AI-ML tabanlı ürün önerisi sonuçlarını yönetme</span><span class="sxs-lookup"><span data-stu-id="f487a-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="f487a-127">Sayfalarına ürün önerileri listesi ekleme</span><span class="sxs-lookup"><span data-stu-id="f487a-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
