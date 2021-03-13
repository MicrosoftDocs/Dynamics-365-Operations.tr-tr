---
title: Ürün önerileri SSS
description: Bu konu, ürün önerilerle veya sonuçları ile ilgili sorunları gidermek için kullanabileceğiniz işlemler ve araçlar hakkında bilgi sağlar.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8eaebaf605cd53ce6848624169c3bbbd2a4281a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009911"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="386b6-103">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="386b6-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="386b6-104">Bu konu, [ürün önerilerle](product-recommendations.md) veya sonuçları ile ilgili sorunları gidermek için kullanabileceğiniz işlemler ve araçlar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="386b6-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="386b6-105">En iyi uygulamalar</span><span class="sxs-lookup"><span data-stu-id="386b6-105">Best practices</span></span>
<span data-ttu-id="386b6-106">Ürün yöneticileri ve türevleri kavramı kullanmak çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="386b6-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="386b6-107">Değişkenlerin ana ürün yöneticisine makul gruplandırması, liste algoritmalarına ve servise daha iyi modeller oluşturmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="386b6-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="386b6-108">Ek olarak, hizmet tüm yakından ilgili varyantları bir listeye koymak yerine yalnızca bir ürünün bir örneğine hizmet edebilir.</span><span class="sxs-lookup"><span data-stu-id="386b6-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="386b6-109">Yakından ilgili tüm varyantlar bir listeye koyulur, hatalı veya tekrarlanan sonuçlar oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="386b6-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="386b6-110">Öneri listemdeki ürünler niçin kayboluyor?</span><span class="sxs-lookup"><span data-stu-id="386b6-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="386b6-111">Genel olarak, ürün öneri listesinde bir madde eksikse, bir ürün konfigürasyonu sorunu olabilir.</span><span class="sxs-lookup"><span data-stu-id="386b6-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="386b6-112">Örneğin, yanlış bir ürün başlangıç tarihi veya bitiş tarihi olabilir, bir boyut yanlış yapılandırılmış olabilir veya ürün doğru kanal sınıflama, vs. olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="386b6-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="386b6-113">Yapay bilgi işlem makinesi öğrenmeyi (AI-ML) temel alan öneri listesinde bir madde eksikse, bu madde öneri listesinin ölçütlerine uygun olmayabilir veya öneri listesinin göstermesi için yeterli sayıda satınalma hareketi bulunmayabilir.</span><span class="sxs-lookup"><span data-stu-id="386b6-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="386b6-114">Aşağıdaki adımları denetlemeniz önerilir:</span><span class="sxs-lookup"><span data-stu-id="386b6-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="386b6-115">**HQ'da ürün önerilerinin etkinleştirildiğinden emin olun.**</span><span class="sxs-lookup"><span data-stu-id="386b6-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="386b6-116">Bu servisin nasıl etkinleştirileceği hakkında bilgi için bkz. [Ürün önerilerini etkinleştir](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="386b6-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="386b6-117">**Önemli ürün özelliklerinin ayarlandığından emin olun.**</span><span class="sxs-lookup"><span data-stu-id="386b6-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="386b6-118">Örneğin, ürün sınıflamalar **dahil** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="386b6-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="386b6-119">**Yeni sıralanmış ürünler için, ürün yeni listede görünmeye başlamadan önce 3 saate kadar sürebilir.**</span><span class="sxs-lookup"><span data-stu-id="386b6-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="386b6-120">**Bir ürün hala, en iyi satış, örneğin benzer veya sık satın alan kişiler gibi görünmeye devam ediyorsa, bu ürünün yeterli hareketi olmayabilir.**</span><span class="sxs-lookup"><span data-stu-id="386b6-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="386b6-121">Bu durumda, daha fazla hareketin gerçekleşmesini bekleyebilir, varsayılan öneri listesi parametrelerini güncelleştirebilir veya öneri ürün listesi sonuçlarını değiştirmek için el ile müdahale kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="386b6-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="386b6-122">Öneri parametreleri hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="386b6-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="386b6-123">**Ürünün, liste için öneri ölçütüne uygun olduğundan emin olun.**</span><span class="sxs-lookup"><span data-stu-id="386b6-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="386b6-124">Ürün öneri parametreleri hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="386b6-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="386b6-125">Düşük öneri sonuçlarının geri döndürülüp döndürülmeyeceğini nasıl engelleyebilirim?</span><span class="sxs-lookup"><span data-stu-id="386b6-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="386b6-126">Öneri listeleri, sonuçları üretmek için büyük bir işlem hacmi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="386b6-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="386b6-127">Bu nedenle, kullanıcıların tam geçmiş hareket verileri sağlaması önemlidir.</span><span class="sxs-lookup"><span data-stu-id="386b6-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="386b6-128">Ek olarak, hareket içermeyen veya az sayıda hareketi olmayan ürünler, genellikle **Bunu da sevdiler** veya **sıklıkla birlikte satın almış** sonuçları içermez ve **trend** veya **en iyi satış** öneri listelerinde görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="386b6-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="386b6-129">Bu durum genellikle çok yeni ürünlerde veya az sayıda satın alma eski ürünlerde ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="386b6-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="386b6-130">Sık kullanılan yeni öğeler bu sorunu kolayca çözmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="386b6-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="386b6-131">Aşağıdaki adımları denetlemeniz önerilir:</span><span class="sxs-lookup"><span data-stu-id="386b6-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="386b6-132">**Ürünün, liste için öneri ölçütüne uygun olduğundan emin olun.**</span><span class="sxs-lookup"><span data-stu-id="386b6-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="386b6-133">Ürün öneri parametreleri hakkında daha fazla bilgi için, bkz. AI-ML tabanlı ürün öneri sonuçlarını düzeltme.</span><span class="sxs-lookup"><span data-stu-id="386b6-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="386b6-134">**Ürün yeni ise, ürünün daha fazla hareketi olana kadar öneri listesini değiştirmeyi düşünebilirsiniz.**</span><span class="sxs-lookup"><span data-stu-id="386b6-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="386b6-135">Öneri liste sonuçlarını düzeltme hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="386b6-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="386b6-136">**Ürünün, liste için öneri ölçütüne uygun olduğundan emin olun.**</span><span class="sxs-lookup"><span data-stu-id="386b6-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="386b6-137">Ürün öneri parametreleri hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="386b6-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="386b6-138">**Ürün yeni ise, ürünün daha fazla hareketi olana kadar öneri listesini değiştirmeyi düşünebilirsiniz.**</span><span class="sxs-lookup"><span data-stu-id="386b6-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="386b6-139">Öneri liste sonuçlarını düzeltme hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="386b6-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="386b6-140">Ürünü kaldırabilir, ancak yine de mağazada görebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="386b6-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="386b6-141">Bir iş gerektiğinde algoritmik olarak oluşturulan listeleri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="386b6-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="386b6-142">Ancak, bir ürün öneri listesinden kaldırılırsa, ürün depoda bulunabilir olarak kalacaktır.</span><span class="sxs-lookup"><span data-stu-id="386b6-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="386b6-143">Ürün öneri sonuçlarını düzeltme hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="386b6-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="386b6-144">Bir maddenin depoda keşfedilmesini engellemelisiniz, **madde sınıflamalar** değerini **hariç tut** olarak değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="386b6-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="386b6-145">Bir e-ticaret sayfasına nasıl liste ekleyebilirim?</span><span class="sxs-lookup"><span data-stu-id="386b6-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="386b6-146">E-ticaret Web sitenize ürün öneri sayfaları ekleme hakkında bilgi için, bkz [Sayfalara ürün öneri listeleri ekle](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="386b6-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="386b6-147">POS'un önerilerini nasıl etkinleştirebilirim?</span><span class="sxs-lookup"><span data-stu-id="386b6-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="386b6-148">Ürün önerilerini etkinleştirdikten sonra, kontrol POS ekranına öneriler panelini eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="386b6-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="386b6-149">Daha fazla bilgi için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="386b6-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="386b6-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="386b6-150">Additional resources</span></span>

[<span data-ttu-id="386b6-151">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="386b6-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="386b6-152">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="386b6-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="386b6-153">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="386b6-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="386b6-154">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="386b6-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="386b6-155">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="386b6-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="386b6-156">"Benzer görünümleri araştır" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="386b6-156">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="386b6-157">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="386b6-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="386b6-158">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="386b6-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="386b6-159">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="386b6-159">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="386b6-160">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="386b6-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="386b6-161">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="386b6-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
