---
title: "\"Benzer görünümleri araştır\" önerilerini etkinleştirme"
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta "benzer görünümleri araştır" ürün önerilerinin nasıl etkinleştirileceği açıklanmaktadır.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 06b5721c423330b8840bb546bdb144c3189c25bb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795393"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="e01b2-103">"Benzer görünümleri araştır" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e01b2-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e01b2-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta "benzer görünümleri araştır" ürün önerilerinin nasıl etkinleştirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e01b2-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e01b2-105">Dynamics 365 Commerce' taki "benzer görünümleri araştır" önerileri özelliği, müşterilere görsel olarak benzer ürünler için öneri sağlamak amacıyla yapay zeka ve makine öğreniminden (AI-ML) yararlanır.</span><span class="sxs-lookup"><span data-stu-id="e01b2-105">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="e01b2-106">Commerce'taki tüm perakende kanallarında "benzer görünümleri araştır" önerileri kullanılabilir duruma getirildiğinde, perakendeciler müşterilerin istediklerini kolayca bulmasına yardımcı olarak müşteri memnuniyetini artırabilir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-106">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="e01b2-107">"Benzer görünümleri araştır" önerileri için işlevsellik, perakendecinin ürün kataloğundaki görsel olarak benzer ürünleri bulmak ve önermek için çekirdek ürün varyantlarının ürün görüntülerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e01b2-107">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="e01b2-108">"Benzer görünümler araştır" önerileri hem satış noktasında (POS) hem de e-ticaret deneyimlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-108">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="e01b2-109">Örnek senaryolar</span><span class="sxs-lookup"><span data-stu-id="e01b2-109">Example scenarios</span></span>

- <span data-ttu-id="e01b2-110">Müşteri siyah çizgili bir kazak görüntüler ve benzer kazağın kırmızı rengi için bir öneri alır.</span><span class="sxs-lookup"><span data-stu-id="e01b2-110">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="e01b2-111">Müşteri, başlangıçta görüntülediği ürün yerine önerilen ürünü seçer ve kırmızı renkli benzer ürünler için öneriler alır.</span><span class="sxs-lookup"><span data-stu-id="e01b2-111">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="e01b2-112">Müşteri satın alma işlemi sırasında ilgilendiği bir yüzükle eşleşen küpeler bulmak için "benzer görünümler araştır" önerilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e01b2-112">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="e01b2-113">Commerce Headquarters'da "benzer görünümler araştır" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e01b2-113">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="e01b2-114">Ürün önerileri, yalnızca depolama alanlarını depolama alanını Azure Data Lake Gen2'ye taşıyan Commerce kullanıcıları için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e01b2-115">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="e01b2-115">Prerequisites</span></span>

<span data-ttu-id="e01b2-116">Perakendeciler müşterilere "benzer görünümler araştır" önerileri göstermeye başlamadan önce, iki önkoşul adımı vardır:</span><span class="sxs-lookup"><span data-stu-id="e01b2-116">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="e01b2-117">Commerce Headquarters'da [ürün önerilerini etkinleştirin](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="e01b2-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="e01b2-118">Ortam sunucusunun HTTPS çağrılarını desteklediğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e01b2-118">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="e01b2-119">Öneriler altyapısının ürün görüntülerine erişmesi için perakendecilerin ürün URL'leri oluşturmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-119">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="e01b2-120">Commerce Headquarters'da ürün URL'leri oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-120">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e01b2-121">**Ürün görüntüleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-121">Go to **Product images**.</span></span>
1. <span data-ttu-id="e01b2-122">Eylem bölmesinde, **Medya şablonu tanımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-122">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="e01b2-123">**Medya şablonu tanımla** özellikleri bölmesinde, **Medya URL'leri** altından **URL Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-123">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="e01b2-124">"Benzer görünümleri araştır" önerileri özelliğini etkinleştirdiğinizde, ürün öneri listeleri oluşturma işlemi başlar.</span><span class="sxs-lookup"><span data-stu-id="e01b2-124">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="e01b2-125">Bu listelerin kullanılabilmesi ve çevrimiçi olarak ve POS terminalinde görülebilmesi için bir güne kadar gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-125">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="e01b2-126">Commerce Headquarters'da "benzer görünümleri araştır" önerileri özelliğini etkinleştirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-126">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e01b2-127">**Özellik yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-127">Go to **Feature management**.</span></span>
1. <span data-ttu-id="e01b2-128">Kullanılabilir özellikler listesinde, **Benzer görünümleri araştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-128">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="e01b2-129">Sağ bölmede, hizmeti açmak için **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-129">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="e01b2-130">Aşağıdaki şekilde, Commerce Headquarters'daki **Özellik Yönetimi** sayfasında bulunan **Benzer görünümleri araştır** özelliği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-130">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Commerce Headquarters'daki Özellik Yönetimi sayfasında bulunan Benzer görünümleri araştır özelliği](./media/enableshopsimilarlooks.png)

<span data-ttu-id="e01b2-132">Önceki görevler tamamlandıktan sonra, POS terminalleri otomatik olarak bağlamsal bir **Benzer görünümleri araştır** paneliyle geliştirilir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-132">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="e01b2-133">**Daha fazlasını gör** öğesini seçerek POS terminali kullanıcıları daha fazla filtreleme yapabilecekleri özel bir "benzer görünümleri araştır" sayfasına gidebilir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-133">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="e01b2-134">"Benzer görünümleri araştır" önerileri özelliğini kapatırsanız, diğer ürün önerisi türleri etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="e01b2-134">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="e01b2-135">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="e01b2-135">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="e01b2-136">Commerce site oluşturucusunu kullanarak ürün ayrıntı sayfalarına Benzer görünümleri araştır düğmesi ekleme</span><span class="sxs-lookup"><span data-stu-id="e01b2-136">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="e01b2-137">Commerce Headquarters'da "benzer görünümleri araştır" önerileri özelliğini etkinleştirdikten sonra, Commerce site oluşturucusundaki bir seçenek perakendecilerin herhangi bir ürün ayrıntısı sayfasındaki (PDP) satın alma kutusuna **Benzer görünümleri araştır** düğmesi eklemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e01b2-137">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="e01b2-138">Bu düğmeyi seçen bir müşteri, görsel olarak benzer ürünler döndüren özel bir "benzer görünümleri araştır" sayfasına götürülür.</span><span class="sxs-lookup"><span data-stu-id="e01b2-138">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="e01b2-139">Burada, müşteri ürünleri daha fazla filtrelemek için seçicileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-139">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="e01b2-140">Commerce site oluşturucusunu kullanarak PDP'ye **Benzer görünümleri araştır** düğmesi eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-140">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e01b2-141">Satın alma kutusu modülünü içeren mevcut bir site oluşturucu sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="e01b2-141">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="e01b2-142">Soldaki gezinti bölmesinde satın alma kutusu modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-142">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="e01b2-143">Sağ gezinti bölmesinde, **Benzer Görünümler Araştır Bağlantısını Etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-143">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="e01b2-144">**Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e01b2-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="e01b2-145">Sayfa yayımlandıktan sonra PDP bir **Benzer görünümler araştır** düğmesi içerir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-145">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="e01b2-146">Aşağıdaki şekilde, **Benzer Görünümler Araştır Bağlantısını Etkinleştir** onay kutusu ve site oluşturucudaki bir PDP örneğinde bulunan **Benzer görünümler araştır** düğmesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e01b2-146">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Benzer Görünümler Araştır Bağlantısını Etkinleştir onay kutusu ve site oluşturucudaki bir PDP'deki Benzer görünümler araştır düğmesi](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="e01b2-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e01b2-148">Additional resources</span></span>

[<span data-ttu-id="e01b2-149">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="e01b2-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e01b2-150">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e01b2-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="e01b2-151">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="e01b2-151">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="e01b2-152">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="e01b2-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="e01b2-153">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="e01b2-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e01b2-154">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="e01b2-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="e01b2-155">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e01b2-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="e01b2-156">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="e01b2-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="e01b2-157">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="e01b2-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="e01b2-158">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="e01b2-158">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
