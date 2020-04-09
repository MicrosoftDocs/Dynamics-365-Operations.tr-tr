---
title: Ürün önerileri SSS
description: Bu konu, ürün önerilerle veya sonuçları ile ilgili sorunları gidermek için kullanabileceğiniz işlemler ve araçlar hakkında bilgi sağlar.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2e30d29516dff6b2128e21bfa6e449e396884d00
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154402"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="53b8b-103">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="53b8b-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="53b8b-104">Bu konu, [ürün önerilerle](product-recommendations.md) veya sonuçları ile ilgili sorunları gidermek için kullanabileceğiniz işlemler ve araçlar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="53b8b-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="53b8b-105">En iyi uygulamalar</span><span class="sxs-lookup"><span data-stu-id="53b8b-105">Best practices</span></span>
<span data-ttu-id="53b8b-106">Ürün yöneticileri ve türevleri kavramı kullanmak çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="53b8b-107">Değişkenlerin ana ürün yöneticisine makul gruplandırması, liste algoritmalarına ve servise daha iyi modeller oluşturmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="53b8b-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="53b8b-108">Ek olarak, hizmet tüm yakından ilgili varyantları bir listeye koymak yerine yalnızca bir ürünün bir örneğine hizmet edebilir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="53b8b-109">Yakından ilgili tüm varyantlar bir listeye koyulur, hatalı veya tekrarlanan sonuçlar oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="53b8b-110">Öneri listemdeki ürünler niçin kayboluyor?</span><span class="sxs-lookup"><span data-stu-id="53b8b-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="53b8b-111">Genel olarak, ürün öneri listesinde bir madde eksikse, bir ürün konfigürasyonu sorunu olabilir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="53b8b-112">Örneğin, yanlış bir ürün başlangıç tarihi veya bitiş tarihi olabilir, bir boyut yanlış yapılandırılmış olabilir veya ürün doğru kanal sınıflama, vs. olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="53b8b-113">Yapay bilgi işlem makinesi öğrenmeyi (AI-ML) temel alan öneri listesinde bir madde eksikse, bu madde öneri listesinin ölçütlerine uygun olmayabilir veya öneri listesinin göstermesi için yeterli sayıda satınalma hareketi bulunmayabilir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="53b8b-114">Aşağıdaki adımları denetlemeniz önerilir:</span><span class="sxs-lookup"><span data-stu-id="53b8b-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="53b8b-115">**HQ'da ürün önerilerinin etkinleştirildiğinden emin olun.**</span><span class="sxs-lookup"><span data-stu-id="53b8b-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="53b8b-116">Bu servisin nasıl etkinleştirileceği hakkında bilgi için bkz. [Ürün önerilerini etkinleştir](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="53b8b-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="53b8b-117">**Önemli ürün özelliklerinin ayarlandığından emin olun.**</span><span class="sxs-lookup"><span data-stu-id="53b8b-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="53b8b-118">Örneğin, ürün sınıflamalar **dahil** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="53b8b-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="53b8b-119">**Yeni sıralanmış ürünler için, ürün yeni listede görünmeye başlamadan önce 3 saate kadar sürebilir.**</span><span class="sxs-lookup"><span data-stu-id="53b8b-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="53b8b-120">**Bir ürün hala, en iyi satış, örneğin benzer veya sık satın alan kişiler gibi görünmeye devam ediyorsa, bu ürünün yeterli hareketi olmayabilir.**</span><span class="sxs-lookup"><span data-stu-id="53b8b-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="53b8b-121">Bu durumda, daha fazla hareketin gerçekleşmesini bekleyebilir, varsayılan öneri listesi parametrelerini güncelleştirebilir veya öneri ürün listesi sonuçlarını değiştirmek için el ile müdahale kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53b8b-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="53b8b-122">Öneri parametreleri hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="53b8b-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="53b8b-123">**Ürünün, liste için öneri ölçütüne uygun olduğundan emin olun.**</span><span class="sxs-lookup"><span data-stu-id="53b8b-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="53b8b-124">Ürün öneri parametreleri hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="53b8b-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="53b8b-125">Düşük öneri sonuçlarının geri döndürülüp döndürülmeyeceğini nasıl engelleyebilirim?</span><span class="sxs-lookup"><span data-stu-id="53b8b-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="53b8b-126">Öneri listeleri, sonuçları üretmek için büyük bir işlem hacmi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="53b8b-127">Bu nedenle, kullanıcıların tam geçmiş hareket verileri sağlaması önemlidir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="53b8b-128">Ek olarak, hareket içermeyen veya az sayıda hareketi olmayan ürünler, genellikle **Bunu da sevdiler** veya **sıklıkla birlikte satın almış** sonuçları içermez ve **trend** veya **en iyi satış** öneri listelerinde görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="53b8b-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="53b8b-129">Bu durum genellikle çok yeni ürünlerde veya az sayıda satın alma eski ürünlerde ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="53b8b-130">Sık kullanılan yeni öğeler bu sorunu kolayca çözmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="53b8b-131">Aşağıdaki adımları denetlemeniz önerilir:</span><span class="sxs-lookup"><span data-stu-id="53b8b-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="53b8b-132">**Ürünün, liste için öneri ölçütüne uygun olduğundan emin olun.**</span><span class="sxs-lookup"><span data-stu-id="53b8b-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="53b8b-133">Ürün öneri parametreleri hakkında daha fazla bilgi için, bkz. AI-ML tabanlı ürün öneri sonuçlarını düzeltme.</span><span class="sxs-lookup"><span data-stu-id="53b8b-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="53b8b-134">**Ürün yeni ise, ürünün daha fazla hareketi olana kadar öneri listesini değiştirmeyi düşünebilirsiniz.**</span><span class="sxs-lookup"><span data-stu-id="53b8b-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="53b8b-135">Öneri liste sonuçlarını düzeltme hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="53b8b-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="53b8b-136">**Ürünün, liste için öneri ölçütüne uygun olduğundan emin olun.**</span><span class="sxs-lookup"><span data-stu-id="53b8b-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="53b8b-137">Ürün öneri parametreleri hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="53b8b-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="53b8b-138">**Ürün yeni ise, ürünün daha fazla hareketi olana kadar öneri listesini değiştirmeyi düşünebilirsiniz.**</span><span class="sxs-lookup"><span data-stu-id="53b8b-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="53b8b-139">Öneri liste sonuçlarını düzeltme hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="53b8b-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="53b8b-140">Ürünü kaldırabilir, ancak yine de mağazada görebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="53b8b-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="53b8b-141">Bir iş gerektiğinde algoritmik olarak oluşturulan listeleri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53b8b-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="53b8b-142">Ancak, bir ürün öneri listesinden kaldırılırsa, ürün depoda bulunabilir olarak kalacaktır.</span><span class="sxs-lookup"><span data-stu-id="53b8b-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="53b8b-143">Ürün öneri sonuçlarını düzeltme hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="53b8b-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="53b8b-144">Bir maddenin depoda keşfedilmesini engellemelisiniz, **madde sınıflamalar** değerini **hariç tut** olarak değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="53b8b-145">Bir e-ticaret sayfasına nasıl liste ekleyebilirim?</span><span class="sxs-lookup"><span data-stu-id="53b8b-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="53b8b-146">E-ticaret Web sitenize ürün öneri sayfaları ekleme hakkında bilgi için, bkz [Sayfalara ürün öneri listeleri ekle](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="53b8b-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="53b8b-147">POS'un önerilerini nasıl etkinleştirebilirim?</span><span class="sxs-lookup"><span data-stu-id="53b8b-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="53b8b-148">Ürün önerilerini etkinleştirdikten sonra, kontrol POS ekranına öneriler panelini eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="53b8b-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="53b8b-149">Daha fazla bilgi için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="53b8b-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53b8b-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="53b8b-150">Additional resources</span></span>

[<span data-ttu-id="53b8b-151">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="53b8b-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="53b8b-152">Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="53b8b-152">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="53b8b-153">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="53b8b-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="53b8b-154">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="53b8b-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="53b8b-155">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="53b8b-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="53b8b-156">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="53b8b-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="53b8b-157">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="53b8b-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="53b8b-158">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="53b8b-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="53b8b-159">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="53b8b-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="53b8b-160">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="53b8b-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
