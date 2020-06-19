---
title: Kişiselleştirilmiş ürün önerileri etkinleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'un müşterileri için kişiselleştirilmiş ürün önerilerinin nasıl yapılacağı açıklanmaktadır.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0e49b4db17ffd792e8dd536a1671773253c74d71
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404152"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="32f4c-103">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="32f4c-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32f4c-104">Bu konuda, Microsoft Dynamics 365 Commerce'un müşterileri için kişiselleştirilmiş ürün önerilerinin nasıl yapılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="32f4c-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="32f4c-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="32f4c-105">Overview</span></span>

<span data-ttu-id="32f4c-106">Dynamics 365 Commerce uygulamasında perakendeciler, kişiselleştirilmiş ürün önerileri (kişiselleştirme olarak da bilinir) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="32f4c-107">Böylece, kişiselleştirilmiş öneriler müşteri deneyimine çevrimiçi ve satış noktasında (POS) dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="32f4c-108">Kişiselleştirme işlevi açıldığında, sistem, bir kullanıcının satın alma ve ürün bilgilerini, kişiselleştirilmemiş ürün önerileri oluşturmak üzere ilişkilendirebilir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="32f4c-109">Kişiselleştirme önkoşulları</span><span class="sxs-lookup"><span data-stu-id="32f4c-109">Personalization prerequisites</span></span>

<span data-ttu-id="32f4c-110">Müşteriler için kişiselleştirilmiş ürün önerileri yapmadan önce, ürün önerilerinin yalnızca depolama alanını Azure Data Lake Store'a geçirmiş olan Commerce Users için desteklendiğini göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="32f4c-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="32f4c-111">Müşteriler kişiselleştirilmiş ürün önerileri alabilmek için, perakendecilerin [ürün önerileriniaçık](enable-product-recommendations.md) olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="32f4c-112">Ürün önerilerini etkinleştirerek, kişiselleştirmeyi de etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="32f4c-113">Ancak, kişiselleştirmeyi kapatırsanız diğer ürün önerisi türlerini kapatmayın.</span><span class="sxs-lookup"><span data-stu-id="32f4c-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="32f4c-114">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="32f4c-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="32f4c-115">Kişiselleştirmeyi açın</span><span class="sxs-lookup"><span data-stu-id="32f4c-115">Turn on personalization</span></span>

<span data-ttu-id="32f4c-116">Kişiselleştirmeyi açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="32f4c-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="32f4c-117">**Perakende ve Ticaret \> ürün önerileri \> öneri parametrelerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="32f4c-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="32f4c-118">Perakende paylaşılan parametreleri listesinde, **öneri listelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="32f4c-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="32f4c-119">**Kişiselleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="32f4c-119">Set the **Enable personalization** option to **Yes**.</span></span>

![Kişiselleştirmeyi açma](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="32f4c-121">Kişiselleştirmeyi etkinleştirdiğinizde, kişiselleştirilmiş ürün önerisi listeleri oluşturma işlemi başlatılır.</span><span class="sxs-lookup"><span data-stu-id="32f4c-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="32f4c-122">Bu listelerin kullanılabilmesi ve çevrimiçi olarak ve POS'ta görülebilmesi için bir güne kadar gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="32f4c-123">Kişiselleştirilmiş listeler</span><span class="sxs-lookup"><span data-stu-id="32f4c-123">Personalized lists</span></span>

<span data-ttu-id="32f4c-124">Öneri Servisi, varolan makine tarafından oluşturulan listelerin kişiselleştirmesine ek olarak, hem çevrimiçi hem de POS'ta ürün bulma deneyiminin kişiselleştirmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="32f4c-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="32f4c-125">Kişiselleştirme etkinleştirildikten sonra, perakendeciler, tüm POS terminallerinde "sizin için özelleştirilmiş" listeler çevrimiçi veya "müşteri" için önerilen "listeleri gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="32f4c-126">Ek olarak, perakendeciler varolan ürün öneri listelerine kişiselleştirmeye uygulayabilir ve kimliği doğrulanmış kullanıcılar için genel veri koruma düzenlemesi (GDPR) geri çevirme deneyimleri sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="32f4c-127">Kişiselleştirmeyi kapatırsanız bu özellikleri de devre dışı bırakırsanız.</span><span class="sxs-lookup"><span data-stu-id="32f4c-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="32f4c-128">Çevrimiçi "sizin için seçilenler" listeleri</span><span class="sxs-lookup"><span data-stu-id="32f4c-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="32f4c-129">"Sizin için seçilenler" listesi, kimliği doğrulanmış bir kullanıcıya önerilen ürünlerin kişiselleştirilmiş bir listesini gösteren yapay bir zekası-makine öğrenme (AI-ML) listesidir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="32f4c-130">Bu liste, kullanıcının çok yönlü kanal satın alma geçmişine dayalıdır.</span><span class="sxs-lookup"><span data-stu-id="32f4c-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="32f4c-131">Kullanıcı başka Satın almalar da yaptığı için, kişiselleştirilmiş öneriler dinamik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="32f4c-132">Bu tür bir liste ayrıca, perakendecilerin Gezinme hiyerarşileri temelinde en üstteki çekmeleri gösterebilmesi için kategori filtrelemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="32f4c-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="32f4c-133">"Sizin için seçilenler" listesi herhangi bir e-ticaret sayfasında görünebileceği için, aşağıdaki kullanıcı gereksinimlerinin karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="32f4c-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="32f4c-134">Kullanıcıların oturum açmış olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-134">Users must be signed in.</span></span> <span data-ttu-id="32f4c-135">Anonim kullanıcılar kişiselleştirilmiş önerileri görmez.</span><span class="sxs-lookup"><span data-stu-id="32f4c-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="32f4c-136">Kullanıcıların hesabında en az bir satın alım olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="32f4c-137">Kullanıcıların kişiselleştirilmiş öneriler almak için kabul olmaları gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="32f4c-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="32f4c-138">Aşağıdaki resimde, bir çevrimiçi mağaza sayfasındaki "sizin için seçilenler" listesinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Çevrimiçi "sizin için seçilenler" listeleri](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="32f4c-140">POS'ta "müşteri için önerilenler" listeleri</span><span class="sxs-lookup"><span data-stu-id="32f4c-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="32f4c-141">Perakendeciler müşteir seçimi deneyimlerini geliştirmek için, varolan müşteri ayrıntıları sayfalarını, bağlamsal bir "müşteri için önerilenler" listesine ekleyerek kişiselleştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="32f4c-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="32f4c-142">Aşağıdaki resimde, bir POS terminalindeki "Müşteri için önerilenler" listesinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![POS'ta "müşteri için önerilenler" listesi](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="32f4c-144">Varolan öneri listelerine kişiselleştirmeyi Uygula</span><span class="sxs-lookup"><span data-stu-id="32f4c-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="32f4c-145">Perakendeciler, "yeni", "trend", "En çok satan", "Bunları da sevdiler" ve "Sıkça birlikte alındı" gibi varolan öneri listelerine kişiselleştirme uygulayabilir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="32f4c-146">Varolan listelere kişiselleştirme uygulandığında, oturum açmış bir kullanıcının önceden satın aldığı öğeler bu listelerden kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="32f4c-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="32f4c-147">Hem anonim kullanıcıların hem de kişiselleştirilmiş öneriler almakla karşılaşan kullanıcıların, varolan listelerin varsayılan sürümleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="32f4c-148">Bu nedenle, perakendeciler, ayrı sayfa deneyimlerini el ile korumak zorunda değildir.</span><span class="sxs-lookup"><span data-stu-id="32f4c-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="32f4c-149">Örneğin, oturum açmış bir Kullanıcı aşağıdaki çizimde yer alan "Trend - varsayılan" listesinde görünen siyah izlemeyi ve kahverengi çalışma ön yüklemeleri 'ni zaten satın aldı.</span><span class="sxs-lookup"><span data-stu-id="32f4c-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="32f4c-150">Bu nedenle, Kullanıcı "Trend - kişiselleştirilmiş" listesinde gösterildiği gibi, bu ürünler yerine yeni ürünler görürler.</span><span class="sxs-lookup"><span data-stu-id="32f4c-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Kişiselleştirme uygulanıyor](./media/applypersonalization.png)

<span data-ttu-id="32f4c-152">Ticaret Sitesi Oluşturmada varolan bir öneri listesine kişiselleştirme uygulamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="32f4c-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="32f4c-153">Ürün toplama modülünü içeren varolan bir site oluşturma sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="32f4c-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="32f4c-154">Soldaki gezinti bölmesinde ürün koleksiyon modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="32f4c-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="32f4c-155">Sağdaki gezinti bölmesinde **Ürünler**'in altında listeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="32f4c-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="32f4c-156">**Ürün listesi konfigürasyonu seç** iletişim kutusunda, **Tür**'ün altında, liste türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="32f4c-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="32f4c-157">**Kişiselleştirmeyi Uygula** onay kutusunu seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="32f4c-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Bir trend listesine kişiselleştirme uygulanıyor](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="32f4c-159">Sayfa parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="32f4c-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="32f4c-160">Sayfa yayımlandıktan sonra, oturum açan kullanıcılar kişiselleştirilmiş liste listeleri görür.</span><span class="sxs-lookup"><span data-stu-id="32f4c-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32f4c-161">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="32f4c-161">Additional resources</span></span>

[<span data-ttu-id="32f4c-162">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="32f4c-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="32f4c-163">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="32f4c-163">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="32f4c-164">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="32f4c-164">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="32f4c-165">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="32f4c-165">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="32f4c-166">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="32f4c-166">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="32f4c-167">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="32f4c-167">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="32f4c-168">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="32f4c-168">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="32f4c-169">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="32f4c-169">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="32f4c-170">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="32f4c-170">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="32f4c-171">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="32f4c-171">Product recommendations FAQ</span></span>](faq-recommendations.md)
