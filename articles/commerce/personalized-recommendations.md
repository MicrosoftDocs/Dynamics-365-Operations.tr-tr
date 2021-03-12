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
ms.openlocfilehash: f535cf0bc3c733426af22cf453ffe97f721f8d9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000596"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="365df-103">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="365df-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="365df-104">Bu konuda, Microsoft Dynamics 365 Commerce'un müşterileri için kişiselleştirilmiş ürün önerilerinin nasıl yapılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="365df-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="365df-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="365df-105">Overview</span></span>

<span data-ttu-id="365df-106">Dynamics 365 Commerce uygulamasında perakendeciler, kişiselleştirilmiş ürün önerileri (kişiselleştirme olarak da bilinir) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="365df-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="365df-107">Böylece, kişiselleştirilmiş öneriler müşteri deneyimine çevrimiçi ve satış noktasında (POS) dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="365df-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="365df-108">Kişiselleştirme işlevi açıldığında, sistem, bir kullanıcının satın alma ve ürün bilgilerini, kişiselleştirilmemiş ürün önerileri oluşturmak üzere ilişkilendirebilir.</span><span class="sxs-lookup"><span data-stu-id="365df-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="365df-109">Kişiselleştirme önkoşulları</span><span class="sxs-lookup"><span data-stu-id="365df-109">Personalization prerequisites</span></span>

<span data-ttu-id="365df-110">Müşteriler için kişiselleştirilmiş ürün önerileri yapmadan önce, ürün önerilerinin yalnızca depolama alanını Azure Data Lake Store'a geçirmiş olan Commerce Users için desteklendiğini göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="365df-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="365df-111">Müşteriler kişiselleştirilmiş ürün önerileri alabilmek için, perakendecilerin [ürün önerileriniaçık](enable-product-recommendations.md) olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="365df-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="365df-112">Ürün önerilerini etkinleştirerek, kişiselleştirmeyi de etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="365df-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="365df-113">Ancak, kişiselleştirmeyi kapatırsanız diğer ürün önerisi türlerini kapatmayın.</span><span class="sxs-lookup"><span data-stu-id="365df-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="365df-114">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="365df-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="365df-115">Kişiselleştirmeyi açın</span><span class="sxs-lookup"><span data-stu-id="365df-115">Turn on personalization</span></span>

<span data-ttu-id="365df-116">Kişiselleştirmeyi açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="365df-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="365df-117">Commerce Headquarters'ta **Özellik Yönetimi**'ni arayın.</span><span class="sxs-lookup"><span data-stu-id="365df-117">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="365df-118">Kullanılabilir özelliklerin listesini görmek için **Tümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="365df-118">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="365df-119">Arama kutusuna **Öneriler** yazın.</span><span class="sxs-lookup"><span data-stu-id="365df-119">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="365df-120">**Kişiselleştirilmiş ürün önerileri** özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="365df-120">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="365df-121">**Kişiselleştirilmiş ürün önerileri** özellikler bölmesinde **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="365df-121">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Kişiselleştirmeyi açma](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="365df-123">Kişiselleştirmeyi etkinleştirdiğinizde, kişiselleştirilmiş ürün önerisi listeleri oluşturma işlemi başlatılır.</span><span class="sxs-lookup"><span data-stu-id="365df-123">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="365df-124">Bu listelerin kullanılabilmesi ve çevrimiçi olarak ve POS'ta görülebilmesi için bir güne kadar gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="365df-124">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="365df-125">Kişiselleştirilmiş listeler</span><span class="sxs-lookup"><span data-stu-id="365df-125">Personalized lists</span></span>

<span data-ttu-id="365df-126">Öneri Servisi, varolan makine tarafından oluşturulan listelerin kişiselleştirmesine ek olarak, hem çevrimiçi hem de POS'ta ürün bulma deneyiminin kişiselleştirmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="365df-126">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="365df-127">Kişiselleştirme etkinleştirildikten sonra, perakendeciler, tüm POS terminallerinde "sizin için özelleştirilmiş" listeler çevrimiçi veya "müşteri" için önerilen "listeleri gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="365df-127">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="365df-128">Ek olarak, perakendeciler varolan ürün öneri listelerine kişiselleştirmeye uygulayabilir ve kimliği doğrulanmış kullanıcılar için genel veri koruma düzenlemesi (GDPR) geri çevirme deneyimleri sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="365df-128">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="365df-129">Kişiselleştirmeyi kapatırsanız bu özellikleri de devre dışı bırakırsanız.</span><span class="sxs-lookup"><span data-stu-id="365df-129">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="365df-130">Çevrimiçi "sizin için seçilenler" listeleri</span><span class="sxs-lookup"><span data-stu-id="365df-130">Online "Picks for you" lists</span></span>

<span data-ttu-id="365df-131">"Sizin için seçilenler" listesi, kimliği doğrulanmış bir kullanıcıya önerilen ürünlerin kişiselleştirilmiş bir listesini gösteren yapay bir zekası-makine öğrenme (AI-ML) listesidir.</span><span class="sxs-lookup"><span data-stu-id="365df-131">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="365df-132">Bu liste, kullanıcının çok yönlü kanal satın alma geçmişine dayalıdır.</span><span class="sxs-lookup"><span data-stu-id="365df-132">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="365df-133">Kullanıcı başka Satın almalar da yaptığı için, kişiselleştirilmiş öneriler dinamik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="365df-133">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="365df-134">Bu tür bir liste ayrıca, perakendecilerin Gezinme hiyerarşileri temelinde en üstteki çekmeleri gösterebilmesi için kategori filtrelemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="365df-134">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="365df-135">"Sizin için seçilenler" listesi herhangi bir e-ticaret sayfasında görünebileceği için, aşağıdaki kullanıcı gereksinimlerinin karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="365df-135">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="365df-136">Kullanıcıların oturum açmış olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="365df-136">Users must be signed in.</span></span> <span data-ttu-id="365df-137">Anonim kullanıcılar kişiselleştirilmiş önerileri görmez.</span><span class="sxs-lookup"><span data-stu-id="365df-137">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="365df-138">Kullanıcıların hesabında en az bir satın alım olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="365df-138">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="365df-139">Kullanıcıların kişiselleştirilmiş öneriler almak için kabul olmaları gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="365df-139">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="365df-140">Aşağıdaki resimde, bir çevrimiçi mağaza sayfasındaki "sizin için seçilenler" listesinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="365df-140">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Çevrimiçi "sizin için seçilenler" listeleri](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="365df-142">POS'ta "müşteri için önerilenler" listeleri</span><span class="sxs-lookup"><span data-stu-id="365df-142">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="365df-143">Perakendeciler müşteir seçimi deneyimlerini geliştirmek için, varolan müşteri ayrıntıları sayfalarını, bağlamsal bir "müşteri için önerilenler" listesine ekleyerek kişiselleştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="365df-143">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="365df-144">Aşağıdaki resimde, bir POS terminalindeki "Müşteri için önerilenler" listesinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="365df-144">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![POS'ta "müşteri için önerilenler" listesi](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="365df-146">Varolan öneri listelerine kişiselleştirmeyi Uygula</span><span class="sxs-lookup"><span data-stu-id="365df-146">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="365df-147">Perakendeciler, "yeni", "trend", "En çok satan", "Bunları da sevdiler" ve "Sıkça birlikte alındı" gibi varolan öneri listelerine kişiselleştirme uygulayabilir.</span><span class="sxs-lookup"><span data-stu-id="365df-147">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="365df-148">Varolan listelere kişiselleştirme uygulandığında, oturum açmış bir kullanıcının önceden satın aldığı öğeler bu listelerden kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="365df-148">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="365df-149">Hem anonim kullanıcıların hem de kişiselleştirilmiş öneriler almakla karşılaşan kullanıcıların, varolan listelerin varsayılan sürümleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="365df-149">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="365df-150">Bu nedenle, perakendeciler, ayrı sayfa deneyimlerini el ile korumak zorunda değildir.</span><span class="sxs-lookup"><span data-stu-id="365df-150">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="365df-151">Örneğin, oturum açmış bir Kullanıcı aşağıdaki çizimde yer alan "Trend - varsayılan" listesinde görünen siyah izlemeyi ve kahverengi çalışma ön yüklemeleri 'ni zaten satın aldı.</span><span class="sxs-lookup"><span data-stu-id="365df-151">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="365df-152">Bu nedenle, Kullanıcı "Trend - kişiselleştirilmiş" listesinde gösterildiği gibi, bu ürünler yerine yeni ürünler görürler.</span><span class="sxs-lookup"><span data-stu-id="365df-152">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Kişiselleştirme uygulanıyor](./media/applypersonalization.png)

<span data-ttu-id="365df-154">Ticaret Sitesi Oluşturmada varolan bir öneri listesine kişiselleştirme uygulamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="365df-154">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="365df-155">Ürün toplama modülünü içeren varolan bir site oluşturma sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="365df-155">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="365df-156">Soldaki gezinti bölmesinde ürün koleksiyon modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="365df-156">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="365df-157">Sağdaki gezinti bölmesinde **Ürünler**'in altında listeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="365df-157">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="365df-158">**Ürün listesi konfigürasyonu seç** iletişim kutusunda, **Tür**'ün altında, liste türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="365df-158">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="365df-159">**Kişiselleştirmeyi Uygula** onay kutusunu seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="365df-159">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Bir trend listesine kişiselleştirme uygulanıyor](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="365df-161">Sayfa parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="365df-161">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="365df-162">Sayfa yayımlandıktan sonra, oturum açan kullanıcılar kişiselleştirilmiş liste listeleri görür.</span><span class="sxs-lookup"><span data-stu-id="365df-162">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="365df-163">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="365df-163">Additional resources</span></span>

[<span data-ttu-id="365df-164">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="365df-164">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="365df-165">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="365df-165">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="365df-166">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="365df-166">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="365df-167">"Benzer görünümleri araştır" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="365df-167">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="365df-168">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="365df-168">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="365df-169">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="365df-169">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="365df-170">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="365df-170">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="365df-171">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="365df-171">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="365df-172">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="365df-172">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="365df-173">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="365df-173">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="365df-174">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="365df-174">Product recommendations FAQ</span></span>](faq-recommendations.md)
