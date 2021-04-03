---
title: Kişiselleştirilmiş ürün önerileri etkinleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'un müşterileri için kişiselleştirilmiş ürün önerilerinin nasıl yapılacağı açıklanmaktadır.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: be460ec5ce8a9a625dc1a80f761bea9e2ab2f632
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477672"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="b7ab3-103">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b7ab3-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b7ab3-104">Bu konuda, Microsoft Dynamics 365 Commerce'un müşterileri için kişiselleştirilmiş ürün önerilerinin nasıl yapılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b7ab3-105">Dynamics 365 Commerce uygulamasında perakendeciler, kişiselleştirilmiş ürün önerileri (kişiselleştirme olarak da bilinir) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="b7ab3-106">Böylece, kişiselleştirilmiş öneriler müşteri deneyimine çevrimiçi ve satış noktasında (POS) dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="b7ab3-107">Kişiselleştirme işlevi açıldığında, sistem, bir kullanıcının satın alma ve ürün bilgilerini, kişiselleştirilmemiş ürün önerileri oluşturmak üzere ilişkilendirebilir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="b7ab3-108">Kişiselleştirme önkoşulları</span><span class="sxs-lookup"><span data-stu-id="b7ab3-108">Personalization prerequisites</span></span>

<span data-ttu-id="b7ab3-109">Müşteriler için kişiselleştirilmiş ürün önerileri yapmadan önce, ürün önerilerinin yalnızca depolama alanını Azure Data Lake Store'a geçirmiş olan Commerce Users için desteklendiğini göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="b7ab3-110">Müşteriler kişiselleştirilmiş ürün önerileri alabilmek için, perakendecilerin [ürün önerileriniaçık](enable-product-recommendations.md) olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b7ab3-111">Ürün önerilerini etkinleştirerek, kişiselleştirmeyi de etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="b7ab3-112">Ancak, kişiselleştirmeyi kapatırsanız diğer ürün önerisi türlerini kapatmayın.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="b7ab3-113">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="b7ab3-114">Kişiselleştirmeyi açın</span><span class="sxs-lookup"><span data-stu-id="b7ab3-114">Turn on personalization</span></span>

<span data-ttu-id="b7ab3-115">Kişiselleştirmeyi açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="b7ab3-116">Commerce Headquarters'ta **Özellik Yönetimi**'ni arayın.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="b7ab3-117">Kullanılabilir özelliklerin listesini görmek için **Tümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="b7ab3-118">Arama kutusuna **Öneriler** yazın.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="b7ab3-119">**Kişiselleştirilmiş ürün önerileri** özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="b7ab3-120">**Kişiselleştirilmiş ürün önerileri** özellikler bölmesinde **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Kişiselleştirmeyi açma](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="b7ab3-122">Kişiselleştirmeyi etkinleştirdiğinizde, kişiselleştirilmiş ürün önerisi listeleri oluşturma işlemi başlatılır.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="b7ab3-123">Bu listelerin kullanılabilmesi ve çevrimiçi olarak ve POS'ta görülebilmesi için bir güne kadar gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="b7ab3-124">Kişiselleştirilmiş listeler</span><span class="sxs-lookup"><span data-stu-id="b7ab3-124">Personalized lists</span></span>

<span data-ttu-id="b7ab3-125">Öneri Servisi, varolan makine tarafından oluşturulan listelerin kişiselleştirmesine ek olarak, hem çevrimiçi hem de POS'ta ürün bulma deneyiminin kişiselleştirmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="b7ab3-126">Kişiselleştirme etkinleştirildikten sonra, perakendeciler, tüm POS terminallerinde "sizin için özelleştirilmiş" listeler çevrimiçi veya "müşteri" için önerilen "listeleri gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="b7ab3-127">Ek olarak, perakendeciler varolan ürün öneri listelerine kişiselleştirmeye uygulayabilir ve kimliği doğrulanmış kullanıcılar için genel veri koruma düzenlemesi (GDPR) geri çevirme deneyimleri sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="b7ab3-128">Kişiselleştirmeyi kapatırsanız bu özellikleri de devre dışı bırakırsanız.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="b7ab3-129">Çevrimiçi "sizin için seçilenler" listeleri</span><span class="sxs-lookup"><span data-stu-id="b7ab3-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="b7ab3-130">"Sizin için seçilenler" listesi, kimliği doğrulanmış bir kullanıcıya önerilen ürünlerin kişiselleştirilmiş bir listesini gösteren yapay bir zekası-makine öğrenme (AI-ML) listesidir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="b7ab3-131">Bu liste, kullanıcının çok yönlü kanal satın alma geçmişine dayalıdır.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="b7ab3-132">Kullanıcı başka Satın almalar da yaptığı için, kişiselleştirilmiş öneriler dinamik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="b7ab3-133">Bu tür bir liste ayrıca, perakendecilerin Gezinme hiyerarşileri temelinde en üstteki çekmeleri gösterebilmesi için kategori filtrelemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="b7ab3-134">"Sizin için seçilenler" listesi herhangi bir e-ticaret sayfasında görünebileceği için, aşağıdaki kullanıcı gereksinimlerinin karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="b7ab3-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="b7ab3-135">Kullanıcıların oturum açmış olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-135">Users must be signed in.</span></span> <span data-ttu-id="b7ab3-136">Anonim kullanıcılar kişiselleştirilmiş önerileri görmez.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="b7ab3-137">Kullanıcıların hesabında en az bir satın alım olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="b7ab3-138">Kullanıcıların kişiselleştirilmiş öneriler almak için kabul olmaları gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="b7ab3-139">Aşağıdaki resimde, bir çevrimiçi mağaza sayfasındaki "sizin için seçilenler" listesinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Çevrimiçi "sizin için seçilenler" listeleri](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="b7ab3-141">POS'ta "müşteri için önerilenler" listeleri</span><span class="sxs-lookup"><span data-stu-id="b7ab3-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="b7ab3-142">Perakendeciler müşteir seçimi deneyimlerini geliştirmek için, varolan müşteri ayrıntıları sayfalarını, bağlamsal bir "müşteri için önerilenler" listesine ekleyerek kişiselleştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="b7ab3-143">Aşağıdaki resimde, bir POS terminalindeki "Müşteri için önerilenler" listesinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![POS'ta "müşteri için önerilenler" listesi](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="b7ab3-145">Varolan öneri listelerine kişiselleştirmeyi Uygula</span><span class="sxs-lookup"><span data-stu-id="b7ab3-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="b7ab3-146">Perakendeciler, "yeni", "trend", "En çok satan", "Bunları da sevdiler" ve "Sıkça birlikte alındı" gibi varolan öneri listelerine kişiselleştirme uygulayabilir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="b7ab3-147">Varolan listelere kişiselleştirme uygulandığında, oturum açmış bir kullanıcının önceden satın aldığı öğeler bu listelerden kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="b7ab3-148">Hem anonim kullanıcıların hem de kişiselleştirilmiş öneriler almakla karşılaşan kullanıcıların, varolan listelerin varsayılan sürümleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="b7ab3-149">Bu nedenle, perakendeciler, ayrı sayfa deneyimlerini el ile korumak zorunda değildir.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="b7ab3-150">Örneğin, oturum açmış bir Kullanıcı aşağıdaki çizimde yer alan "Trend - varsayılan" listesinde görünen siyah izlemeyi ve kahverengi çalışma ön yüklemeleri 'ni zaten satın aldı.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="b7ab3-151">Bu nedenle, Kullanıcı "Trend - kişiselleştirilmiş" listesinde gösterildiği gibi, bu ürünler yerine yeni ürünler görürler.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Kişiselleştirme uygulanıyor](./media/applypersonalization.png)

<span data-ttu-id="b7ab3-153">Ticaret Sitesi Oluşturmada varolan bir öneri listesine kişiselleştirme uygulamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b7ab3-154">Ürün toplama modülünü içeren varolan bir site oluşturma sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="b7ab3-155">Soldaki gezinti bölmesinde ürün koleksiyon modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="b7ab3-156">Sağdaki gezinti bölmesinde **Ürünler**'in altında listeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="b7ab3-157">**Ürün listesi konfigürasyonu seç** iletişim kutusunda, **Tür**'ün altında, liste türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="b7ab3-158">**Kişiselleştirmeyi Uygula** onay kutusunu seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Bir trend listesine kişiselleştirme uygulanıyor](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="b7ab3-160">Sayfa parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="b7ab3-161">Sayfa yayımlandıktan sonra, oturum açan kullanıcılar kişiselleştirilmiş liste listeleri görür.</span><span class="sxs-lookup"><span data-stu-id="b7ab3-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7ab3-162">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b7ab3-162">Additional resources</span></span>

[<span data-ttu-id="b7ab3-163">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="b7ab3-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b7ab3-164">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b7ab3-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b7ab3-165">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="b7ab3-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b7ab3-166">"Benzer görünümleri araştır" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b7ab3-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="b7ab3-167">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="b7ab3-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b7ab3-168">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="b7ab3-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b7ab3-169">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="b7ab3-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b7ab3-170">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="b7ab3-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="b7ab3-171">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="b7ab3-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b7ab3-172">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="b7ab3-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="b7ab3-173">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="b7ab3-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
