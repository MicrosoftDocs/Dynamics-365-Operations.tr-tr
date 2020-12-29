---
title: AI-ML tabanlı ürün önerisi sonuçlarını ayarlama
description: Bu konu, yapay zeka makine öğrenme (AI-ML) tabanlı ürün öneri sonuçlarının işletmenize nasıl uyarlanacağını açıklamaktadır.
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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: bc6a793061a3e644599f0882ff163f5f57b2162d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416511"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="97f2c-103">AI-ML tabanlı ürün önerisi sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="97f2c-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="97f2c-104">Bu konu, yapay zeka makine öğrenme (AI-ML) tabanlı ürün öneri sonuçlarının işletmeniz için nasıl ayarlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="97f2c-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="97f2c-105">Ürün önerilerini etkinleştirdikten sonra, varsayılan ayarlar etkili olur; Bu parametreler birçok gereksinim için çalışır.</span><span class="sxs-lookup"><span data-stu-id="97f2c-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="97f2c-106">Sonuçların satış hareketi ile uyumlu olup olmadıklarını değerlendirmek için bir zaman harcamaya plan yapmak en iyisidir.</span><span class="sxs-lookup"><span data-stu-id="97f2c-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="97f2c-107">Yeniden test etmeden önce parametreleri değiştirmeden önce, birkaç gün için sonuçları değerlendirme öneriyoruz.</span><span class="sxs-lookup"><span data-stu-id="97f2c-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="97f2c-108">Öneri listesi parametrelerini anlama</span><span class="sxs-lookup"><span data-stu-id="97f2c-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="97f2c-109">Parametreleri değiştirmeden önce, aşağıdaki sonuçların nasıl etkilendiklerini öğrenin.</span><span class="sxs-lookup"><span data-stu-id="97f2c-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="97f2c-110">"Trend" ürün listesi</span><span class="sxs-lookup"><span data-stu-id="97f2c-110">"Trending" product list</span></span>

<span data-ttu-id="97f2c-111">"Trend" ürün listesi, değiştirilebilen iki parametreye sahiptir:</span><span class="sxs-lookup"><span data-stu-id="97f2c-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Örnek "Trend" listesi varsayılan parametresi](./media/exampletrendingparameters.png)

1. <span data-ttu-id="97f2c-113">**Son X günden yeni ürünleri dahil et** - Ürün adaylarını seçmek için geçerli tarihten önce belirtilen gün sayısına eklenen ürünler.</span><span class="sxs-lookup"><span data-stu-id="97f2c-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="97f2c-114">Resimdeki varsayılan değer, ürünlerin eski ürün listesinde 180 gün içinde kullanılabilir olmasını önerir.</span><span class="sxs-lookup"><span data-stu-id="97f2c-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="97f2c-115">**Son X günden satışları dahil et** - Ürün sipariş etmek için geçerli tarihten önce belirtilen gün sayısındaki satış işlemleri.</span><span class="sxs-lookup"><span data-stu-id="97f2c-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="97f2c-116">Yukarıdaki varsayılan değer, son 30 gün içinde bir ürünün yaptığı tüm satınalmaların, ürünün trend ürün listesine yerleştirilmesiyle ilgili olarak kullanılmasını önerir.</span><span class="sxs-lookup"><span data-stu-id="97f2c-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="97f2c-117">"Trend" ürün listesi</span><span class="sxs-lookup"><span data-stu-id="97f2c-117">"Best selling" product list</span></span>

<span data-ttu-id="97f2c-118">İşinize bağlı olarak "En iyi satış" listesi, her ikisi de sipariş ürünleri için hareket verileri kullansa bile, daha fazla satan sonuçlar elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="97f2c-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="97f2c-119">En iyi satış, sınıflama tarihine bağlı olarak kesilmediğinden, en iyi satış çok popüler olan, trend listesinden düşmüş olan daha eski ürünleri vurgulayabilir.</span><span class="sxs-lookup"><span data-stu-id="97f2c-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="97f2c-120">"En iyi satış" ürün listesi, değiştirilebilen bir parametreye sahiptir:</span><span class="sxs-lookup"><span data-stu-id="97f2c-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Örnek en iyi satış listesi varsayılan parametresi](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="97f2c-122">**Son X günden satışları dahil et** - Ürün sipariş etmek için geçerli tarihten önce belirtilen gün sayısındaki satış işlemleri.</span><span class="sxs-lookup"><span data-stu-id="97f2c-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="97f2c-123">Yukarıdaki varsayılan değer, son 30 gün içinde bir ürünün yaptığı tüm satınalmaların, ürünün en iyi satış çok popüler olan ürün listesine yerleştirilmesiyle ilgili olarak kullanılmasını önerir.</span><span class="sxs-lookup"><span data-stu-id="97f2c-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="97f2c-124">Öneri listelerine el ile ürün ekleme veya kaldırma</span><span class="sxs-lookup"><span data-stu-id="97f2c-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="97f2c-125">"Yeni", "trend" veya "en İyi satış" listeleri için</span><span class="sxs-lookup"><span data-stu-id="97f2c-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="97f2c-126">**Perakende ve Ticaret** > **ürün önerileri** > **öneri parametrelerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="97f2c-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="97f2c-127">Paylaşılan parametreleri listesinde, **öneri listelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="97f2c-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="97f2c-128">Ürünlerin ekleneceği veya kaldırılacağı listeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="97f2c-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="97f2c-129">Tabloya ürün eklemek için **Satır ekle** seçin.</span><span class="sxs-lookup"><span data-stu-id="97f2c-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="97f2c-130">Ürün sütunu altında, **adı** veya **ürün numarasını** kullanarak ürünü arayın.</span><span class="sxs-lookup"><span data-stu-id="97f2c-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Yeni ürün listesinde ürün arama örneği](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="97f2c-132">Satır türü sütunu altında, iki seçenekten birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="97f2c-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="97f2c-133">**Dahil et** – bir ürünü listenin önüne zorlar</span><span class="sxs-lookup"><span data-stu-id="97f2c-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="97f2c-134">**Dışla** – bir ürünün listede görünmesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="97f2c-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Ürünü yeni ürün listesinden içerme veya hariç tutma örneği](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="97f2c-136">**Görüntüleme sırasının** değiştirilmesi, **dahil** edilen ürünlerin listede görüneceği sırayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="97f2c-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="97f2c-137">İki ürün aynı **görüntü sipariş** değerine sahipse, bu iki sonucun son sırası arka ofisten farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="97f2c-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="97f2c-138">Tablodan ürün kaldırmak için: kaldırılacak satırı seçin ve **Kaldır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="97f2c-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="97f2c-139">"Bunları da beğenenler" ve "Birlikte sık satın alınanlar" listeleri için</span><span class="sxs-lookup"><span data-stu-id="97f2c-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="97f2c-140">"Sıklıkla birlikte satın alınanlar" veya "Bunları da beğendiler" listeleri bağlamında, makine öğrenme, özel bir üretim ürünü için yaygın olarak satın alınan ilgili ürünleri önermek amacıyla tüketici satın alma düzenlerini analiz etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="97f2c-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="97f2c-141">*Tohum ürünü*, sonuçları oluşturmak istediğiniz ürün.</span><span class="sxs-lookup"><span data-stu-id="97f2c-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="97f2c-142">Öneri listelerini el ile ayarlama bağlamında, bu ürün için sonuç ekliyor veya kaldırırsınız.</span><span class="sxs-lookup"><span data-stu-id="97f2c-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="97f2c-143">Bir çekirdek ürünle ilgili sonuçları el ile eklemek veya kaldırmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="97f2c-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="97f2c-144">**Tohum ürünü** seçin.</span><span class="sxs-lookup"><span data-stu-id="97f2c-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="97f2c-145">**Ürün** sütunu altında, **adı** veya **ürün numarasını** kullanarak ürünü arayın.
![Yeni ürün listesinde ürün arama örneği](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="97f2c-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="97f2c-146">**Satır türü** sütunu altında, iki seçenekten birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="97f2c-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="97f2c-147">**Dahil et** – bir ürünü listenin önüne zorlar</span><span class="sxs-lookup"><span data-stu-id="97f2c-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="97f2c-148">**Dışla** – bir ürünün listede görünmesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="97f2c-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="97f2c-149">![En sık satın alınan listede ürün ekleme veya çıkarma örneği](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="97f2c-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="97f2c-150">Tablodan ürün kaldırmak için: kaldırılacak satırı seçin ve Kaldır 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="97f2c-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="97f2c-151">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="97f2c-151">Additional resources</span></span>

[<span data-ttu-id="97f2c-152">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="97f2c-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="97f2c-153">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="97f2c-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="97f2c-154">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="97f2c-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="97f2c-155">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="97f2c-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="97f2c-156">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="97f2c-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="97f2c-157">"Benzer görünümleri araştır" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="97f2c-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="97f2c-158">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="97f2c-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="97f2c-159">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="97f2c-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="97f2c-160">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="97f2c-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="97f2c-161">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="97f2c-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="97f2c-162">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="97f2c-162">Product recommendations FAQ</span></span>](faq-recommendations.md)
