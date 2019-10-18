---
title: POS'ta ürün önerileri
description: Bu konuda bir satış noktasında (POS) ürün önerilerinin nasıl kullanılacağı açıklanmaktadır.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278404"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="5d20d-103">POS'ta ürün önerileri</span><span class="sxs-lookup"><span data-stu-id="5d20d-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d20d-104">Temel olarak ürün önerileri; zengin, çekici ve özel ürün keşfi deneyimleri oluşturmak amacıyla tüm perakende alanlara yayılan, dönüştürülebilir iş uygulamasıdır.</span><span class="sxs-lookup"><span data-stu-id="5d20d-104">At its core, product Recommendations are a transformative business application that span across all retail spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="5d20d-105">Bu özelliği POS'ta uygulamak için [POS cihazlarınıza öneri ekleme](add-recommendations-control-pos-screen.md) başlıklı makaledeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5d20d-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="5d20d-106">Ürün önerileri özelliği hakkında daha fazla bilgi edinmek için [ürün önerilerine genel bakış](../commerce/product-recommendations.md) başlıklı makaleyi okuyun.</span><span class="sxs-lookup"><span data-stu-id="5d20d-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="5d20d-107">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="5d20d-107">Scenarios</span></span>

<span data-ttu-id="5d20d-108">Ürün önerileri aşağıdaki POS senaryoları için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="5d20d-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="5d20d-109">Bulut POS veya Modern POS'da (MPOS) kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5d20d-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="5d20d-110">**Ürün ayrıntıları** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="5d20d-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="5d20d-111">• Bir mağaza çalışanı farklı kanallardan gerçekleştirilen önceki hareketlere bakarken **Ürün ayrıntıları** sayfasını ziyaret ederse öneriler hizmeti, birlikte satın alınabilecek ek maddeleri önerir.</span><span class="sxs-lookup"><span data-stu-id="5d20d-111">• If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="5d20d-112">[![Ürün ayrıntıları sayfasında öneriler](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="5d20d-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="5d20d-113">**Hareket** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="5d20d-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="5d20d-114">• Öneri altyapısı, sepetteki sıklıkla birlikte satın alınan tüm maddeler listesine dayalı olarak madde önerir.</span><span class="sxs-lookup"><span data-stu-id="5d20d-114">• The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5d20d-115">**Hareket** sayfasında önerileri görüntülemek için, perakendecinin Dynamics 365 for Retail'da ekran düzenini güncelleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5d20d-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="5d20d-116">**Öneriler** denetimi, **Hareket** sayfasına geçirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="5d20d-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="5d20d-117">[![Hareketler sayfasında öneriler](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="5d20d-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a><span data-ttu-id="5d20d-118">POS önerilerini etkinleştirmek için Dynamics 365 Retail yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5d20d-118">Configure Dynamics 365 Retail to enable POS recommendations</span></span>

<span data-ttu-id="5d20d-119">Ürün önerilerini ayarlamak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5d20d-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="5d20d-120">Hizmetinizin **10.0.6 derlemesine** güncelleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="5d20d-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="5d20d-121">İşletmeniz için [ürün önerilerini etkinleştirme](../commerce/enable-product-recommendations.md) yönergelerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="5d20d-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="5d20d-122">İsteğe bağlı: Hareket ekranında önerileri görüntülemek için **Ekran düzeni**'ne gidin ekran düzeninizi seçin, **Ekran düzeni tasarımcısı**'nı başlatın ve sonra **öneriler** denetimini gereken yere bırakın.</span><span class="sxs-lookup"><span data-stu-id="5d20d-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="5d20d-123">**Perakende parametreleri**'ne gidin, **Makine öğrenimi**'ni seçin, **POS önerilerini etkinleştir** altından **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="5d20d-123">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="5d20d-124">Önerileri POS'ta görmek için genel yapılandırma işini **1110** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="5d20d-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="5d20d-125">Yapılan değişiklikleri POS ekran düzeni tasarımcısına yansıtmak için, kanal yapılandırma işini **1070** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="5d20d-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="5d20d-126">Zaten etkinleştirilmiş ürün önerileriyle ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="5d20d-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="5d20d-127">**Perakende Parametreleri** \> **Öneri listeleri** \> **Ürün önerilerini devre dışı bırak**'a gidip **Genel yapılandırma işi \[9999\]**'u çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="5d20d-127">Navigate to **Retail Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="5d20d-128">**Öneriler denetimini** hareket ekranınıza **Ekran düzeni tasarımcısını** kullanarak eklediyseniz bunu da kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5d20d-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="5d20d-129">Ek sorularınız varsa daha fazla bilgi edinmek için [Önerilerle ilgili SSS](../commerce/faq-recommendations.md) başlıklı makaleye göz atın.</span><span class="sxs-lookup"><span data-stu-id="5d20d-129">If you have additional questions, check out the [Recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d20d-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5d20d-130">Additional resources</span></span>

<span data-ttu-id="5d20d-131">[Bir POS cihazındaki hareket sayfasına öneriler denetimini ekleme](add-recommendations-control-pos-screen.md)
[Ürün önerilerine genel bakış](../commerce/product-recommendations.md)
[Ürün önerilerini etkinleştirme](../commerce/enable-product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="5d20d-131">[Add a recommendations control to the transaction page on a POS device](add-recommendations-control-pos-screen.md)
[Product recommendations overview](../commerce/product-recommendations.md)
[Enable product recommendations](../commerce/enable-product-recommendations.md)</span></span> 
