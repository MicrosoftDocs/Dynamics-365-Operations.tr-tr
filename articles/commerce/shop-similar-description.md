---
title: "\"Benzer ürünler açıklaması\" önerilerini etkinleştirme"
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta "benzer ürünler açıklaması" ürün önerilerinin nasıl etkinleştirileceği açıklanmaktadır.
author: bsokolov
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ce01ef1d4b916d955685b4d01dafd3d54d6fcebd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795417"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="d6059-103">"Benzer ürünler açıklaması" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d6059-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6059-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta "benzer ürünler açıklaması" ürün önerilerinin nasıl etkinleştirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d6059-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d6059-105">Dynamics 365 Commerce'teki "benzer ürünler açıklaması" önerileri özelliği, müşterinin aradığı açıklamaya benzer açıklamalara sahip ürünler için öneriler sunmak üzere yapay zeka ve makine öğrenimi (AI-ML) kullanır.</span><span class="sxs-lookup"><span data-stu-id="d6059-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="d6059-106">Commerce'teki tüm perakende kanallarında "benzer ürün açıklaması" önerileri kullanılabilir duruma getirildiğinde, perakendeciler müşterilerin istediklerini kolayca bulmasına yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="d6059-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="d6059-107">"Benzer ürün açıklaması" önerileri için işlevsellik, perakendecinin ürün kataloğundaki benzer ürünleri bulmak ve önermek için çekirdek ürünlerin ürün adını ve açıklamasını kullanır.</span><span class="sxs-lookup"><span data-stu-id="d6059-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="d6059-108">"Benzer ürün açıklaması" önerileri hem satış noktasında (POS) hem de e-ticaret deneyimlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d6059-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="d6059-109">Örnek senaryolar</span><span class="sxs-lookup"><span data-stu-id="d6059-109">Example scenarios</span></span>

<span data-ttu-id="d6059-110">Aşağıdaki örnek senaryolar, "Benzer ürün açıklaması" işlevinin sağlayabileceği öneri türlerini gösterir:</span><span class="sxs-lookup"><span data-stu-id="d6059-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="d6059-111">Bir müşteri, bir dizi retro, kemik tipi gözlük görüntüler ve benzeri bir tasarıma sahip diğer gözlükler için satıcının sektörü bağlamında bir dizi öneri alır.</span><span class="sxs-lookup"><span data-stu-id="d6059-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="d6059-112">Bir müşteri, daha önce perakendeciden satın aldıkları bir tadla benzerlik gösteren kahve tadlarını bulmak için "benzer ürün açıklaması" önerilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d6059-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="d6059-113">"Benzer ürünler açıklaması" önerilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="d6059-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="d6059-114">Ürün önerileri, yalnızca depolama alanlarını depolama alanını Azure Data Lake Storage Gen2'ye taşıyan Commerce kullanıcıları için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="d6059-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d6059-115">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="d6059-115">Prerequisites</span></span>

<span data-ttu-id="d6059-116">"Benzeri ürün açıklaması" önerilerini müşterilere göre gösterilebilmeniz için aşağıdaki önkoşulları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="d6059-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="d6059-117">Commerce Headquarters'da [ürün önerilerini etkinleştirin](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d6059-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="d6059-118">Ortam sunucusunun HTTPS çağrılarını desteklediğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d6059-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="d6059-119">"Benzer ürün açıklaması" önerileri özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d6059-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="d6059-120">Commerce Headquarters'da "benzer ürün açıklaması" önerileri özelliğini etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d6059-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d6059-121">**Özellik yönetimi** çalışma alanında, kullanılabilen özellikler listesinde, **Benzer ürün açıklaması**'nı arayıp seçin.</span><span class="sxs-lookup"><span data-stu-id="d6059-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="d6059-122">Sağdaki bölmeden **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6059-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="d6059-123">Özelliği etkinleştirdiğinizde, sistem, ürün öneri listeleri oluşturmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="d6059-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="d6059-124">Bu listelerin kullanılabilmesi ve çevrimiçi olarak ve POS terminalinde görülebilmesi bir gün sürebilir.</span><span class="sxs-lookup"><span data-stu-id="d6059-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="d6059-125">Bu özelliği kapatırsanız diğer ürün önerisi türleri etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="d6059-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="d6059-126">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="d6059-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="d6059-127">Ürün ayrıntıları sayfalarına, Benzer ürün açıklaması düğmesi ekleyin</span><span class="sxs-lookup"><span data-stu-id="d6059-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="d6059-128">Commerce Headquarters'da "benzer ürün açıklaması" önerileri özelliğini etkinleştirdikten sonra, herhangi bir ürün ayrıntısı sayfasındaki (PDP) satın alma kutusuna **Benzer ürün açıklaması** düğmesi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6059-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="d6059-129">Bu düğmeyi seçen bir müşteri, görsel olarak benzer ürünler gösteren özel bir **Benzer ürün açıklaması** sayfasına götürülür.</span><span class="sxs-lookup"><span data-stu-id="d6059-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="d6059-130">Müşteri ürünleri daha fazla filtrelemek için seçicileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="d6059-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="d6059-131">Commerce site oluşturucusunu kullanarak PDP'ye **Benzer ürün açıklaması** düğmesi eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d6059-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d6059-132">Satın alma kutusu modülünü içeren mevcut bir site oluşturucu sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="d6059-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="d6059-133">Soldaki gezinti bölmesinde satın alma kutusu modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="d6059-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="d6059-134">Sağ bölmede, **Benzer ürün açıklaması bağlantısını etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d6059-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="d6059-135">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6059-135">Select **Save**.</span></span>
1. <span data-ttu-id="d6059-136">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6059-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="d6059-137">Sayfa yayımlandıktan sonra PDP bir **Benzer ürün açıklaması** düğmesi içerir.</span><span class="sxs-lookup"><span data-stu-id="d6059-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="d6059-138">Aşağıdaki şekilde, **Benzer ürün açıklaması Bağlantısını Etkinleştir** onay kutusu ve site oluşturucudaki bir PDP örneğinde bulunan **Benzer ürün açıklaması** düğmesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d6059-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Benzer ürün açıklaması Bağlantısını Etkinleştir onay kutusu ve site oluşturucudaki bir PDP'deki Benzer ürün açıklaması düğmesi](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="d6059-140">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d6059-140">Additional resources</span></span>

[<span data-ttu-id="d6059-141">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="d6059-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d6059-142">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d6059-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d6059-143">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="d6059-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d6059-144">"Benzer görünümdeki mağaza" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d6059-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="d6059-145">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="d6059-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d6059-146">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="d6059-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d6059-147">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="d6059-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]