---
title: AI-ML tabanlı ürün önerisi sonuçlarını yönetme
description: Bu konu, yapay zeka makine öğrenme (AI-ML) tabanlı ürün öneri sonuçlarının işletmenize nasıl uyarlanacağını açıklamaktadır.
author: bebeale
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
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770082"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="0c107-103">AI-ML tabanlı ürün önerisi sonuçlarını yönetme</span><span class="sxs-lookup"><span data-stu-id="0c107-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0c107-104">Bu konu, yapay zeka makine öğrenme (AI-ML) tabanlı ürün öneri sonuçlarının işletmenize nasıl uyarlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0c107-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="0c107-105">Ürün önerilerini etkinleştirdikten sonra, varsayılan ayarlar etkili olur; Bu parametreler birçok gereksinim için çalışır.</span><span class="sxs-lookup"><span data-stu-id="0c107-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="0c107-106">Sonuçların satış hareketi ile uyumlu olup olmadıklarını değerlendirmek için bir zaman harcamaya plan yapmak en iyisidir.</span><span class="sxs-lookup"><span data-stu-id="0c107-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="0c107-107">Yeniden test etmeden önce parametreleri değiştirmeden önce, birkaç gün için sonuçları değerlendirme öneriyoruz.</span><span class="sxs-lookup"><span data-stu-id="0c107-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="0c107-108">Öneri listesi parametrelerini anlama</span><span class="sxs-lookup"><span data-stu-id="0c107-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="0c107-109">Parametreleri değiştirmeden önce, aşağıdaki sonuçların nasıl etkilendiklerini öğrenin.</span><span class="sxs-lookup"><span data-stu-id="0c107-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="0c107-110">Trend ürün listesi</span><span class="sxs-lookup"><span data-stu-id="0c107-110">Trending product list</span></span>

<span data-ttu-id="0c107-111">**Trend** ürün listesi, değiştirilebilecek iki parametreye sahiptir: ![örnek trend listesi varsayılan parametreler](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="0c107-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="0c107-112">**Son X günden yeni ürünleri dahil et** - Ürün adaylarını seçmek için geçerli tarihten önce belirtilen gün sayısına eklenen ürünler.</span><span class="sxs-lookup"><span data-stu-id="0c107-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="0c107-113">Resimdeki varsayılan değer, ürünlerin eski ürün listesinde 180 gün içinde kullanılabilir olmasını önerir.</span><span class="sxs-lookup"><span data-stu-id="0c107-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="0c107-114">**Son X günden satışları dahil et** - Ürün sipariş etmek için geçerli tarihten önce belirtilen gün sayısındaki satış işlemleri.</span><span class="sxs-lookup"><span data-stu-id="0c107-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="0c107-115">Yukarıdaki varsayılan değer, son 30 gün içinde bir ürünün yaptığı tüm satınalmaların, ürünün trend ürün listesine yerleştirilmesiyle ilgili olarak kullanılmasını önerir.</span><span class="sxs-lookup"><span data-stu-id="0c107-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="0c107-116">En iyi satış ürün listesi</span><span class="sxs-lookup"><span data-stu-id="0c107-116">Best selling product list</span></span>

<span data-ttu-id="0c107-117">İşinize bağlı olarak en iyi satış, her ikisi de sipariş ürünleri için hareket verileri kullansa bile, daha fazla satan sonuçlar elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="0c107-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="0c107-118">En iyi satış, sınıflama tarihine bağlı olarak kesilmediğinden, en iyi satış çok popüler olan, trend listesinden düşmüş olan daha eski ürünleri vurgulayabilir.</span><span class="sxs-lookup"><span data-stu-id="0c107-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="0c107-119">**En iyi satış** ürün listesi, değiştirilebilen bir parametreye sahiptir:</span><span class="sxs-lookup"><span data-stu-id="0c107-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Örnek en iyi satış listesi varsayılan parametresi](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="0c107-121">**Son X günden satışları dahil et** - Ürün sipariş etmek için geçerli tarihten önce belirtilen gün sayısındaki satış işlemleri.</span><span class="sxs-lookup"><span data-stu-id="0c107-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="0c107-122">Yukarıdaki varsayılan değer, son 30 gün içinde bir ürünün yaptığı tüm satınalmaların, ürünün en iyi satış çok popüler olan ürün listesine yerleştirilmesiyle ilgili olarak kullanılmasını önerir.</span><span class="sxs-lookup"><span data-stu-id="0c107-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="0c107-123">Öneri listelerine el ile ürün ekleme veya kaldırma</span><span class="sxs-lookup"><span data-stu-id="0c107-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="0c107-124">Yeni, trend veya en İyi satış için</span><span class="sxs-lookup"><span data-stu-id="0c107-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="0c107-125">**Perakende** > **ürün önerileri** > **öneri parametrelerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="0c107-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="0c107-126">Perakende paylaşılan parametreleri listesinde, **öneri listelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="0c107-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="0c107-127">Ürünlerin ekleneceği veya kaldırılacağı listeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c107-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="0c107-128">Tabloya ürün eklemek için **Satır ekle** seçin.</span><span class="sxs-lookup"><span data-stu-id="0c107-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="0c107-129">Ürün sütunu altında, **adı** veya **ürün numarasını** kullanarak ürünü arayın. 
![Yeni ürün listesinde ürün arama örneği](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="0c107-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="0c107-130">Satır türü sütunu altında, iki seçenekten birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="0c107-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="0c107-131">**Dahil et** – bir ürünü listenin önüne zorlar</span><span class="sxs-lookup"><span data-stu-id="0c107-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="0c107-132">**Hariç tut** – ürünün liste görünmesini kaldırır ![Yeni ürün listesinden bir ürün dahil etme ya da çıkarma örneği](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="0c107-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="0c107-133">**Görüntüleme sırasının** değiştirilmesi, **dahil** edilen ürünlerin listede görüneceği sırayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0c107-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="0c107-134">İki ürün aynı **görüntü sipariş** değerine sahipse, bu iki sonucun son sırası arka ofisten farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0c107-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="0c107-135">Tablodan ürün kaldırmak için: kaldırılacak satırı seçin ve **Kaldır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c107-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="0c107-136">Bunları da beğenenler ve Birlikte sık satın alınanlar listeleri için</span><span class="sxs-lookup"><span data-stu-id="0c107-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="0c107-137">**Sıklıkla birlikte satın alınanlar** veya **Bunları da beğendiler** listeleri bağlamında, makine öğrenme, özel bir üretim ürünü için yaygın olarak satın alınan ilgili ürünleri önermek amacıyla tüketici satın alma düzenlerini analiz etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0c107-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="0c107-138">**Tohum ürünü**, sonuçları oluşturmak istediğiniz ürün.</span><span class="sxs-lookup"><span data-stu-id="0c107-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="0c107-139">Öneri listelerini el ile ayarlama bağlamında, bu ürün için sonuç ekliyor veya kaldırırsınız.</span><span class="sxs-lookup"><span data-stu-id="0c107-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="0c107-140">Bir çekirdek ürünle ilgili sonuçları el ile eklemek veya kaldırmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="0c107-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="0c107-141">**Tohum ürünü** seçin.</span><span class="sxs-lookup"><span data-stu-id="0c107-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="0c107-142">**Ürün** sütunu altında, **adı** veya **ürün numarasını** kullanarak ürünü arayın.
![Yeni ürün listesinde ürün arama örneği](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="0c107-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="0c107-143">**Satır türü** sütunu altında, iki seçenekten birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="0c107-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="0c107-144">**Dahil et** – bir ürünü listenin önüne zorlar</span><span class="sxs-lookup"><span data-stu-id="0c107-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="0c107-145">**Dışla** – bir ürünün listede görünmesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="0c107-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="0c107-146">![En sık satın alınan listede ürün ekleme veya çıkarma örneği](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="0c107-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="0c107-147">Tablodan ürün kaldırmak için: kaldırılacak satırı seçin ve Kaldır 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c107-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="0c107-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0c107-148">Additional resources</span></span>

[<span data-ttu-id="0c107-149">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="0c107-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="0c107-150">Ürün önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0c107-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="0c107-151">Sayfalarına ürün önerileri listesi ekleme</span><span class="sxs-lookup"><span data-stu-id="0c107-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
