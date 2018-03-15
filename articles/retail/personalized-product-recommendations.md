---
title: "Kişiselleştirilmiş ürün önerilerine genel bakış"
description: "Bu konuda satış noktası (POS) cihazında görüntülenebilecek Dynamics 365 for Retail ürün önerileri hakkında bilgiler yer almaktadır."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 16bdf2176869e5822ddf8732c829b65f1e60632c
ms.openlocfilehash: ce91f675082a34bd5a1e88be7a7af6884dc47add
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="41ecd-103">Kişiselleştirilmiş ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="41ecd-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="41ecd-104">Bu özelliği daha iyi bir algoritma ve daha yeni perakende odaklı yeteneklerle yeniden tasarladığımızdan ürün öneri hizmetinin geçerli sürümünü kaldırıyoruz.</span><span class="sxs-lookup"><span data-stu-id="41ecd-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="41ecd-105">Daha fazla bilgi için bkz. [Kaldırılan veya artık kullanılmayan özellikler](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="41ecd-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="41ecd-106">Dynamics 365 for Retail'da, ürün önerileri satış noktası cihazında (POS) görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-106">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="41ecd-107">Öneriler satınalma geçmişi, istek listelerindeki maddeler ve diğer müşterilerin çevrimiçi ve fiziksel mağazalardan aldıkları maddelere dayanarak müşterilerin ilgi duyabilecekleri maddelerdir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-107">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="41ecd-108">Büyük kataloglara sahip perakendeciler için öneriler müşterinin ürün bulmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="41ecd-108">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="41ecd-109">Müşterinin ilgi alanlarını ve satın alma alışkanlıklarını hedefleyen ürünleri sunarak , ürün önerileri perakendecilere çapraz satış ve yukarı satış konusunda yardımı olabilir ve müşteri tutmayı geliştirebilir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-109">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="41ecd-110">Dynamics 365 for Retail'de ürün önerileri bilişsel hizmetler ve Microsoft Azure makine öğrenimiyle desteklenir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-110">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="41ecd-111">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="41ecd-111">Scenarios</span></span>
---------

<span data-ttu-id="41ecd-112">Ürün önerileri aşağıdaki POS senaryoları için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-112">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="41ecd-113">Bulut POS veya Modern POS'da (MPOS) kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-113">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="41ecd-114">**Ürün ayrıntıları** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="41ecd-114">On the **Product details** page:</span></span>

-   <span data-ttu-id="41ecd-115">Bir mağaza çalışanı farklı kanallardan gerçekleştirilen önceki hareketlere bakarken **Ürün ayrıntıları** sayfasını ziyaret ederse, öneri altyapısı birlikte satın alınabilecek ek maddeleri önerir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-115">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="41ecd-116">Mağaza çalışanı müşteriyi harekete ekler ve **Ürün ayrıntıları** sayfasını ziyaret ederse, öneri altyapısı müşteri hareket geçmişini kullanarak kişiselleştirilmiş öneriler sağlar.</span><span class="sxs-lookup"><span data-stu-id="41ecd-116">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="41ecd-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="41ecd-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="41ecd-118">**Hareket** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="41ecd-118">On the **Transaction** page:</span></span>

-   <span data-ttu-id="41ecd-119">Öneri altyapısı sepetteki maddelerin tam listesini temel olarak maddeler önerir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-119">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="41ecd-120">Mağaza çalışanı müşteriyi harekete eklerse, öneri altyapısı müşteri hareket geçmişini ve sepetteki maddelerin listesini kullanarak kişiselleştirilmiş öneriler sağlar.</span><span class="sxs-lookup"><span data-stu-id="41ecd-120">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="41ecd-121">**Hareket** sayfasında önerileri görüntülemek için, perakendecinin Dynamics 365 for Retail'da ekran düzenini güncelleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-121">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="41ecd-122">**Öneriler** denetimi, **Hareket** sayfasında atlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="41ecd-122">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="41ecd-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="41ecd-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="41ecd-124">**Müşteri ayrıntıları** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="41ecd-124">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="41ecd-125">Öneri altyapısı Kullanıcı kimliğini ve müşteri istek listesindeki maddeleri temel olarak maddeler önerir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-125">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="41ecd-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="41ecd-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="41ecd-127">Dynamics 365 for Retail'ı POS önerileri etkinleştirme işlemleri için yapılandırma</span><span class="sxs-lookup"><span data-stu-id="41ecd-127">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="41ecd-128">Ürün önerilerini ayarlamak için aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="41ecd-128">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="41ecd-129">Doğru **Tüzel kişilik** seçimi yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="41ecd-129">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="41ecd-130">**Varlık deposu**'na gidin, **Perakende satış**'ı seçin ve ardından **Yenile**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41ecd-130">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="41ecd-131">Bu, işlem veritabanınızdan alınan demo verileri (veya sizin verilerinizi) kullanır ve bunu Varlık deposuna taşır.</span><span class="sxs-lookup"><span data-stu-id="41ecd-131">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="41ecd-132">İsteğe bağlı: Hareket ekranında önerileri görüntülemek için **Ekran düzeni**'ne gidin ekran düzeninizi seçin, **Ekran düzeni tasarımcısı**'nı başlatın ve sonra **öneriler** denetimini gereken yere bırakın.</span><span class="sxs-lookup"><span data-stu-id="41ecd-132">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="41ecd-133">**Perakende parametreleri**'ne gidin, **Makine öğrenimi**'ni seçin, **POS önerilerini etkinleştir** altından **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="41ecd-133">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="41ecd-134">Önerileri POS'ta görmek için genel yapılandırma işini **1110** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="41ecd-134">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="41ecd-135">Yapılan değişiklikleri POS ekran düzeni tasarımcısına yansıtmak için, kanal yapılandırma işini **1070** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="41ecd-135">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="41ecd-136">[]()Nasıl çalışır?</span><span class="sxs-lookup"><span data-stu-id="41ecd-136">[]()How does it work?</span></span>
<span data-ttu-id="41ecd-137">**Varlık deposu** varlığını yenilediğinizde, aşağıdaki eylemleri gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-137">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="41ecd-138">Bilişsel hizmetler tarafından istenen biçimdeki veriler Dynamics 365 for Retail işlem veritabanından çıkarılır ve Varlık deposuna gönderilir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-138">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="41ecd-139">Veriler, Azure Data Factory (ADF) tarafından ADF etkinliklerinin bir parçası olarak Hive betiği kullanan verileri temizlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41ecd-139">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="41ecd-140">Temizlenen veriler blob depolamada saklanır.</span><span class="sxs-lookup"><span data-stu-id="41ecd-140">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="41ecd-141">Blob depolamadaki veriler öneri modelini eğitmek amacıyla Bilişsel hizmetler API'sı tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41ecd-141">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="41ecd-142">**Önerileri etkinleştir**'i açıp yapılandırma işlerini çalıştırdığınızda, aşağıdaki eylemler gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-142">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="41ecd-143">Model kimlik bilgileri ve kimliği API'dan toplanır ve Dynamics 365 for Retail işlem veritabanında, AOS için web.config'de ve ayrıca perakende sunucusunda depolanır.</span><span class="sxs-lookup"><span data-stu-id="41ecd-143">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="41ecd-144">Model kimlik bilgileri ve kimliği CRT'nin kullanımına sunulur, böylece Bulut POS ve MPOS'tan çevrimiçi modda gelen ürün önerileri çağrıları değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="41ecd-144">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="41ecd-145">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="41ecd-145">See also</span></span>
--------

[<span data-ttu-id="41ecd-146">POS cihazındaki hareket sayfasına öneriler denetimi ekleme</span><span class="sxs-lookup"><span data-stu-id="41ecd-146">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




