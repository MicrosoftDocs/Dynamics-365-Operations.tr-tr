---
title: POS'ta ürün önerileri ekleme
description: Bu konuda bir satış noktasında (POS) ürün önerilerinin nasıl kullanılacağı açıklanmaktadır.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48533596c5bdc73dd8c815166e7dde0ca2f3cb4d
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127825"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="a6993-103">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="a6993-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a6993-104">Temel olarak ürün önerileri; zengin, çekici ve özel ürün keşfi deneyimleri oluşturmak amacıyla tüm ticari alanlara yayılan, dönüştürülebilir iş uygulamasıdır.</span><span class="sxs-lookup"><span data-stu-id="a6993-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="a6993-105">Bu özelliği POS'ta uygulamak için [POS cihazlarınıza öneri ekleme](add-recommendations-control-pos-screen.md) başlıklı makaledeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a6993-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="a6993-106">Ürün önerileri özelliği hakkında daha fazla bilgi edinmek için [ürün önerilerine genel bakış](../commerce/product-recommendations.md) başlıklı makaleyi okuyun.</span><span class="sxs-lookup"><span data-stu-id="a6993-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="a6993-107">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="a6993-107">Scenarios</span></span>

<span data-ttu-id="a6993-108">Ürün önerileri aşağıdaki POS senaryoları için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a6993-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="a6993-109">Bulut POS veya Modern POS'da (MPOS) kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a6993-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="a6993-110">**Ürün ayrıntıları** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="a6993-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="a6993-111">Mağaza çalışanı farklı kanallardan gerçekleştirilen önceki hareketlere bakarken **Ürün ayrıntıları** sayfasını ziyaret ederse öneriler hizmeti, birlikte satın alınabilecek ek maddeleri önerir.</span><span class="sxs-lookup"><span data-stu-id="a6993-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="a6993-112">[![Ürün ayrıntıları sayfasında öneriler](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="a6993-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="a6993-113">**Hareket** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="a6993-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="a6993-114">Öneri altyapısı, sepetteki sıklıkla birlikte satın alınan tüm maddeler listesine göre madde önerir.</span><span class="sxs-lookup"><span data-stu-id="a6993-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a6993-115">**Hareket** sayfasında önerileri görüntülemek için, perakendecinin Dynamics 365 Commerce'da ekran düzenini güncelleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a6993-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a6993-116">**Öneriler** denetimi, **Hareket** sayfasına geçirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a6993-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="a6993-117">[![Hareketler sayfasında öneriler](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="a6993-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="a6993-118">POS önerilerini etkinleştirmek için Commerce yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a6993-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="a6993-119">Ürün önerilerini ayarlamak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="a6993-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="a6993-120">Hizmetinizin **10.0.6 derlemesine** güncelleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="a6993-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="a6993-121">İşletmeniz için [ürün önerilerini etkinleştirme](../commerce/enable-product-recommendations.md) yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="a6993-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="a6993-122">İsteğe bağlı: Hareket ekranında önerileri görüntülemek için **Ekran düzeni**'ne gidin ekran düzeninizi seçin, **Ekran düzeni tasarımcısı**'nı başlatın ve sonra **öneriler** denetimini gereken yere bırakın.</span><span class="sxs-lookup"><span data-stu-id="a6993-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="a6993-123">**Commerce parametreleri**'ne gidin, **Makine öğrenimi**'ni seçin, **POS önerilerini etkinleştir** altından **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a6993-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="a6993-124">Önerileri POS'ta görmek için genel yapılandırma işini **1110** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a6993-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="a6993-125">Yapılan değişiklikleri POS ekran düzeni tasarımcısına yansıtmak için, kanal yapılandırma işini **1070** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a6993-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="a6993-126">Zaten etkinleştirilmiş ürün önerileriyle ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="a6993-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="a6993-127">**Commerce Parametreleri** \> **Öneri listeleri** \> **Ürün önerilerini devre dışı bırak**'a gidip **Genel yapılandırma işi \[9999\]**'u çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a6993-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="a6993-128">**Öneriler denetimini** hareket ekranınıza **Ekran düzeni tasarımcısını** kullanarak eklediyseniz bunu da kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a6993-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="a6993-129">Başka sorularınız olursa daha fazla bilgi edinmek için [Ürün önerileri SSS](../commerce/faq-recommendations.md) başlıklı makaleye göz atın.</span><span class="sxs-lookup"><span data-stu-id="a6993-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6993-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a6993-130">Additional resources</span></span>

[<span data-ttu-id="a6993-131">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="a6993-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a6993-132">Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a6993-132">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a6993-133">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="a6993-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a6993-134">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a6993-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a6993-135">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="a6993-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a6993-136">e-Ticaret sitesine önerisi listeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="a6993-136">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="a6993-137">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="a6993-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a6993-138">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="a6993-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a6993-139">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="a6993-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a6993-140">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="a6993-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a6993-141">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="a6993-141">Product recommendations FAQ</span></span>](faq-recommendations.md)
