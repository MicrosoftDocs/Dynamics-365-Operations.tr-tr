---
title: Ürün önerilerine genel bakış
description: Bu konuda ürün önerileri hakkında genel bilgiler verilmiştir. Ürün önerileri, müşterilerin istedikleri ürünleri ve hatta satın almayı amaçlamadıkları ürünleri kolayca ve hızlı bir şekilde bulmasına olanak tanır.
author: Moonma
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 044a5c21e4ebf1bf83edc74335e655b9388bc1d4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795609"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="0c6de-104">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="0c6de-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c6de-105">Microsoft Dynamics 365 Commerce, e-ticaret Web sitesi ve satış noktası (POS) aygıtında ürün önerilerini göstermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="0c6de-106">Ürün önerileri, bir müşterinin ilgilendiği öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="0c6de-107">Öneriler, çevrimiçi ve fiziksel mağazalardaki diğer müşterilerin satın alma eğilimlerine dayanır.</span><span class="sxs-lookup"><span data-stu-id="0c6de-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="0c6de-108">Ürün önerileri, müşterilerin kendilerine hizmet veren bir deneyim sağlarken istedikleri ürünleri kolayca ve hızlı bir şekilde bulmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0c6de-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="0c6de-109">Çapraz satış ve yukarı satış, müşterilerin başlangıçta satın almayı amaçlamadıkları ek ürünler bulmasına yardımcı olmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="0c6de-110">Öneriler, ürün bulmayı geliştirmek için kullanıldığında, daha fazla dönüştürme fırsatı oluşturabilir, satış gelirini artırabilir ve hatta müşteri memnuniyetini ve korunmasını bile yükseltebilir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="0c6de-111">e-Ticarette, ürün önerileri büyük ölçekli Microsoft önerileri makine öğrenme teknolojileriyle desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="0c6de-112">Öneri servisi</span><span class="sxs-lookup"><span data-stu-id="0c6de-112">Recommendation service</span></span>

<span data-ttu-id="0c6de-113">Ürün önerileri hizmeti, yapay zeka ve makine öğrenimi (AI-ML) teknolojilerini aşağıdaki şekilde kullanır:</span><span class="sxs-lookup"><span data-stu-id="0c6de-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="0c6de-114">Öneri servisinin tarafından istenen biçimdeki veriler Commerce işlem veritabanından çıkarılması ve Azure Data Lake Storage veya Varlık deposuna göndermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="0c6de-115">Öneriler hizmeti, depolanan verileri **Bunlar da beğenildi**, **Sıklıkla birlikte satın alınan**, **Yeni**, **En çok satan** ve **Popüler** listeleri için öneri modelleri eğitmek üzere kullanır.</span><span class="sxs-lookup"><span data-stu-id="0c6de-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="0c6de-116">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="0c6de-116">Scenarios</span></span>

<span data-ttu-id="0c6de-117">Ürün önerileri aşağıdaki senaryoları için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="0c6de-118">**E-ticaret 'da gözatma veya iniş sayfası için herhangi bir depolama sayfasında:** Müşteriler veya mağaza işbirlikçileri bir mağaza sayfasını ziyaret ederken, öneri altyapısı **yeni**, **en iyi satış** ve **trend** listelerinde ürünler önerebilir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="0c6de-119">**Ürün Ayrıntıları sayfasında:** müşteriler veya mağaza işbirlikçileri bir **ürün ayrıntıları** sayfasını ziyaret ederken, öneri altyapısı da büyük olasılıkla satın alınacak ek maddeleri önerir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="0c6de-120">Bu öğeler, **kişiler bunları da sevdi** listesinde görünür.</span><span class="sxs-lookup"><span data-stu-id="0c6de-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="0c6de-121">**Hareket sayfasında veya kullanıma al sayfasında:** öneri altyapısı maddeleri sepetteki tüm madde listesine göre önerir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="0c6de-122">Bu maddeler **sık kullanılan bir arada** bulunan listesinde görünür.</span><span class="sxs-lookup"><span data-stu-id="0c6de-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="0c6de-123">**Kişiselleştirilmiş öneriler:** Tacirler, varolan liste senaryolarının o müşteriye dayalı olarak kişiselleştirilmelerini sağlayan yeni işlevlere ek olarak, oturum açmış, **sizin için kişiselleştirilmiş** bir çekme müşterilerine olanak sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="0c6de-124">Daha fazla bilgi edinmek için bkz. [Kişiselleştirilmiş önerileri etkinleştirme.](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="0c6de-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="0c6de-125">Ürün önerileri türleri</span><span class="sxs-lookup"><span data-stu-id="0c6de-125">Types of product recommendations</span></span>

<span data-ttu-id="0c6de-126">Aşağıdaki tabloda, perakendecilerin Dynamics 365 Commerce çözümlerinde [ürün koleksiyonu modülü](product-collection-module-overview.md) aracılığıyla uygulayabilecekleri için çeşitli otomatik ürün önerisi türleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0c6de-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="0c6de-127">Perakendeciler site yazarı bu seçeneği seçerse, oturum açmış bir kullanıcının kişiselleştirilmiş sonuçlarını gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="0c6de-128">Ürün topluluğu modülü</span><span class="sxs-lookup"><span data-stu-id="0c6de-128">Product collection module</span></span>  | <span data-ttu-id="0c6de-129">Türü</span><span class="sxs-lookup"><span data-stu-id="0c6de-129">Type</span></span> | <span data-ttu-id="0c6de-130">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c6de-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="0c6de-131">Yeni</span><span class="sxs-lookup"><span data-stu-id="0c6de-131">New</span></span>                        | <span data-ttu-id="0c6de-132">Algoritmik</span><span class="sxs-lookup"><span data-stu-id="0c6de-132">Algorithmic</span></span> | <span data-ttu-id="0c6de-133">Bu modül, kanallarda ve kataloglarda yakın zamanda sıralanmış en yeni ürünlerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="0c6de-134">En iyi satış</span><span class="sxs-lookup"><span data-stu-id="0c6de-134">Best selling</span></span>               | <span data-ttu-id="0c6de-135">Algoritmik</span><span class="sxs-lookup"><span data-stu-id="0c6de-135">Algorithmic</span></span> | <span data-ttu-id="0c6de-136">Bu modül, en yüksek sayıda satış ile derecelendirilen ürünlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="0c6de-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="0c6de-137">Popüler</span><span class="sxs-lookup"><span data-stu-id="0c6de-137">Trending</span></span>                   | <span data-ttu-id="0c6de-138">Algoritmik</span><span class="sxs-lookup"><span data-stu-id="0c6de-138">Algorithmic</span></span> | <span data-ttu-id="0c6de-139">Bu modül belirli bir döneme ait en yüksek performanslı ürünlerin listesini, en yüksek satış sayısına göre sıralayarak gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="0c6de-140">Sıklıkla birlikte satın alınan</span><span class="sxs-lookup"><span data-stu-id="0c6de-140">Frequently bought together</span></span> | <span data-ttu-id="0c6de-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="0c6de-141">AI-ML</span></span> | <span data-ttu-id="0c6de-142">Bu modül, tüketicilerin geçerli sepet içeriğiyle birlikte yaygın olarak satın alınan ürünlerin listesini önerir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="0c6de-143">Diğer sevilen ürünler</span><span class="sxs-lookup"><span data-stu-id="0c6de-143">People also like</span></span>           | <span data-ttu-id="0c6de-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="0c6de-144">AI-ML</span></span> | <span data-ttu-id="0c6de-145">Bu modül, tüketicinin satın alma modellerine dayalı olarak, belirli bir temel ürün için ürünler önerir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="0c6de-146">Size özel çekmeler</span><span class="sxs-lookup"><span data-stu-id="0c6de-146">Picks for you</span></span>              | <span data-ttu-id="0c6de-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="0c6de-147">AI-ML</span></span> | <span data-ttu-id="0c6de-148">Bu modül, oturum açmış kullanıcının satınalma kalıplarını temel alan kişiselleştirilmiş bir ürün listesi önerir.</span><span class="sxs-lookup"><span data-stu-id="0c6de-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="0c6de-149">Konuk Kullanıcı için bu liste daraltılacak.</span><span class="sxs-lookup"><span data-stu-id="0c6de-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="0c6de-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0c6de-150">Additional resources</span></span>

[<span data-ttu-id="0c6de-151">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0c6de-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="0c6de-152">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="0c6de-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="0c6de-153">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0c6de-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="0c6de-154">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="0c6de-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="0c6de-155">"Benzer görünümleri araştır" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0c6de-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="0c6de-156">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="0c6de-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="0c6de-157">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="0c6de-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="0c6de-158">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="0c6de-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="0c6de-159">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c6de-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="0c6de-160">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c6de-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="0c6de-161">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="0c6de-161">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]