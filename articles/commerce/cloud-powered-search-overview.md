---
title: Bulut destekli aramaya genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'ta bulut destekli aramanın genel görünümünü vermektedir.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5501f4d39709990eb352511477b1427fb265afde
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057845"
---
# <a name="cloud-powered-search-overview"></a><span data-ttu-id="ed090-103">Bulut destekli aramaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="ed090-103">Cloud-powered search overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ed090-104">Bu konu, Microsoft Dynamics 365 Commerce'ta bulut destekli aramanın genel görünümünü vermektedir.</span><span class="sxs-lookup"><span data-stu-id="ed090-104">This topic gives an overview of cloud-powered search in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ed090-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="ed090-105">Overview</span></span>

<span data-ttu-id="ed090-106">Ürün bulunabilirliği, müşterilerin kategorilerine, aramaya ve filtre uygulamasına göre hızlı ve kolay bir şekilde ürünleri bulabilmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ed090-106">Product discoverability helps guarantee that customers can quickly and easily find products by browsing categories, searching, and filtering.</span></span> <span data-ttu-id="ed090-107">Perakendeciler, tüm kanallarda müşteri etkileşimi için ürün keşfini bir ana araç olarak kabul edin.</span><span class="sxs-lookup"><span data-stu-id="ed090-107">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span>

<span data-ttu-id="ed090-108">Müşteriler, arama terimleri yazarken, çok yönlü gezinme ve vurgulamadan, Web arama altyapılarının, gelişmiş e-ticaret web sitelerinin, sosyal uygulamaların ve otomatik önerilerin neredeyse anlık yanıt sürelerine alışkın olurlar.</span><span class="sxs-lookup"><span data-stu-id="ed090-108">Customers are accustomed to the nearly instantaneous response times of web search engines, sophisticated e-Commerce websites, social apps, automatic suggestions that appear as they type search terms, faceted navigation, and highlighting.</span></span> <span data-ttu-id="ed090-109">Müşteriler, istedikleri ürünü bir e-ticaret mağazasında hızlı bulamayacakları takdirde, farklı bir e-ticaret deposuna gitmekten çekinmeyin.</span><span class="sxs-lookup"><span data-stu-id="ed090-109">If customers can't find the product that they are looking for quickly enough in one e-Commerce store, they won't hesitate to go to a different e-Commerce store.</span></span>

<span data-ttu-id="ed090-110">Dynamics 365 Commerce'teki bulut destekli ürün bulunabilirliği, perakendecilere, hem e-ticaret kanalları hem de satış noktası (POS) kanalları gibi tüm kanallardaki tüketici bekletmesi ve dönüştürme oranlarını artırmak için devam etmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ed090-110">The cloud-powered product discoverability in Dynamics 365 Commerce helps retailers continue to increase consumer retention and conversion rates across all channels, both e-Commerce channels and point of sale (POS) channels.</span></span>

<span data-ttu-id="ed090-111">Dynamics 365 Commerce arama deneyiminin, perakendecilere daha iyi ürün bulunabilirliği elde etmenize yardımcı olacak yetenekler geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ed090-111">The Dynamics 365 Commerce search experience has improved capabilities to help retailers achieve better product discoverability.</span></span> <span data-ttu-id="ed090-112">Aynı zamanda, bu yetenekler e-ticaret trafiği için gerekli ölçeklenebilirliği ve performansı sağlar.</span><span class="sxs-lookup"><span data-stu-id="ed090-112">At the same time, these capabilities deliver the scalability and performance that are required for e-Commerce traffic.</span></span>

## <a name="browse-and-search"></a><span data-ttu-id="ed090-113">Tarama ve arama</span><span class="sxs-lookup"><span data-stu-id="ed090-113">Browse and search</span></span>

<span data-ttu-id="ed090-114">Ürün bulma işlemi öncelikle bilgi alımı ve içerik gezintisi için arama işlevleriyle ilgili olduğundan, arama ilgisi ve performansı, çoklu kanal deneyiminde önemli etkenlerdir.</span><span class="sxs-lookup"><span data-stu-id="ed090-114">Search relevance and performance are key factors in the omnichannel experience, because product discovery relies primarily on search functionality for information retrieval and content navigation.</span></span> <span data-ttu-id="ed090-115">Etkili ve etkin bir gözatma ve arama deneyimi dönüştürmenin artmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ed090-115">An effective and efficient browse and search experience helps increase conversion.</span></span>

<span data-ttu-id="ed090-116">Aşağıdaki çizimde, tipik gözatma ve arama işlevlerinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ed090-116">The following illustration shows an example of typical browse and search functionality.</span></span>

![Arama giriş sayfası](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a><span data-ttu-id="ed090-118">Çok yönlü gezinme ve seçim Özeti</span><span class="sxs-lookup"><span data-stu-id="ed090-118">Faceted navigation and choice summary</span></span> 

<span data-ttu-id="ed090-119">Çok yönlü gezinme, müşterilerin bir terim kümesindeki terimlerle bağlantılı iyileştiricilerin filtrelerine izin vererek içeriğe daha kolay gözatmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ed090-119">Faceted navigation helps customers more easily browse for content by letting them filter on refiners that are linked to terms in a term set.</span></span> <span data-ttu-id="ed090-120">Müşteri iyileştiriciler seçtikten ve uygulandıktan sonra, seçeneklerin özeti gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ed090-120">After a customer has selected and applied refiners, a summary of the choices is shown.</span></span> 

<span data-ttu-id="ed090-121">Çok yönlü gezinme kullanarak, ek sayfalar oluşturmak zorunda kalmadan terim kümesindeki farklı terimler için farklı iyileştiricileri konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed090-121">By using faceted navigation, you can configure different refiners for different terms in a term set, without having to create additional pages.</span></span> 

<span data-ttu-id="ed090-122">Aşağıdaki çizimde, çok yönlü gezintinin aramada kullanıldığı bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ed090-122">The following illustration shows an example where faceted navigation is used in a search.</span></span>

![Seçim özeti](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a><span data-ttu-id="ed090-124">Derinlikli otomatik önerme</span><span class="sxs-lookup"><span data-stu-id="ed090-124">Immersive autosuggest</span></span>

<span data-ttu-id="ed090-125">Geçerli otomatik öneri işlevselliği yalnızca eşleşen anahtar sözcüğü aramayı tetikleyen anahtar sözcükleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed090-125">Current autosuggest functionality just shows keywords that trigger a search for the matching keyword.</span></span> <span data-ttu-id="ed090-126">Dynamics 365 Commerce'teki yeni geliştirmeler nedeniyle, müşteriler yazma işlemi tamamlanmadan önce ürün bağlantılarını sıkça bulabilir.</span><span class="sxs-lookup"><span data-stu-id="ed090-126">Because of new enhancements in Dynamics 365 Commerce, customers can often discover links to products before they have finished typing.</span></span>

<span data-ttu-id="ed090-127">Dynamics 365 Commerce ayrıca çeşitli kategorilerdeki anahtar sözcük eşleşmeleri işlevselliğini destekler.</span><span class="sxs-lookup"><span data-stu-id="ed090-127">Dynamics 365 Commerce also supports functionality for keyword matches in various categories.</span></span> <span data-ttu-id="ed090-128">Bu işlevsellik, müşterilerin kategoriler arasında eşleşen anahtar sözcüklerin sayısını görmesini ve diğer kategorilerdeki bir anahtar sözcükle ilgili arama tetiklemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ed090-128">This functionality lets customers see the number of matching keywords across categories and trigger a search for a keyword in other categories.</span></span>

<span data-ttu-id="ed090-129">Aşağıdaki çizimde, derinlikli otomatik önerinin kullanıldığı bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ed090-129">The following illustration shows an example where immersive autosuggest is being used.</span></span>

![derinlikli otomatik önerme](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a><span data-ttu-id="ed090-131">Sırala</span><span class="sxs-lookup"><span data-stu-id="ed090-131">Sort</span></span>

<span data-ttu-id="ed090-132">Müşterilerimize, Dynamics 365 Commerce geliştirilmiş sıralama; arama sonuçlarını sıralama, arama ve gözatma ve fiyat, ürün adı ve ürün numarası gibi ölçütlere göre bunları belirginleştirme.</span><span class="sxs-lookup"><span data-stu-id="ed090-132">Enhanced sorting in Dynamics 365 Commerce lets customers sort, search, and browse search results, and refine them by criteria such as price, product name, and product number.</span></span> <span data-ttu-id="ed090-133">Müşteriler Ayrıca, ürünün yeni, en çok satılan veya son eklenen bir ürün olup olmadığına göre sonuçları sıralayabilir.</span><span class="sxs-lookup"><span data-stu-id="ed090-133">Customers can also sort results based on whether a product is new, top-selling, or recently added.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed090-134">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ed090-134">Additional resources</span></span>

[<span data-ttu-id="ed090-135">Varsayılan kategori giriş sayfası ve arama sonuçları sayfası</span><span class="sxs-lookup"><span data-stu-id="ed090-135">Default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="ed090-136">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="ed090-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)
