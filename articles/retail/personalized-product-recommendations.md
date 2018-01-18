---
title: "Kişiselleştirilmiş ürün önerilerine genel bakış"
description: "Bu konuda satış noktası (POS) cihazında görüntülenebilecek Dynamics 365 for Retail ürün önerileri hakkında bilgiler yer almaktadır."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: eddd9cdf7cf45dafe5b6142ad0069f1248fee2bf
ms.contentlocale: tr-tr
ms.lasthandoff: 01/18/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="eeef9-103">Kişiselleştirilmiş ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="eeef9-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="eeef9-104">Bu özellik şu anda yalnızca korumalı alan ve üretim (yüksek kullanılabilirlik) dağıtım topolojilerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-104">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="eeef9-105">Dynamics 365 for Retail'da, ürün önerileri satış noktası cihazında (POS) görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-105">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="eeef9-106">Öneriler satınalma geçmişi, istek listelerindeki maddeler ve diğer müşterilerin çevrimiçi ve fiziksel mağazalardan aldıkları maddelere dayanarak müşterilerin ilgi duyabilecekleri maddelerdir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-106">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="eeef9-107">Büyük kataloglara sahip perakendeciler için öneriler müşterinin ürün bulmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="eeef9-107">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="eeef9-108">Müşterinin ilgi alanlarını ve satın alma alışkanlıklarını hedefleyen ürünleri sunarak , ürün önerileri perakendecilere çapraz satış ve yukarı satış konusunda yardımı olabilir ve müşteri tutmayı geliştirebilir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-108">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="eeef9-109">Dynamics 365 for Retail'de ürün önerileri bilişsel hizmetler ve Microsoft Azure makine öğrenimiyle desteklenir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-109">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="eeef9-110">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="eeef9-110">Scenarios</span></span>
---------

<span data-ttu-id="eeef9-111">Ürün önerileri aşağıdaki POS senaryoları için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-111">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="eeef9-112">Bulut POS veya Modern POS'da (MPOS) kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-112">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="eeef9-113">**Ürün ayrıntıları** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="eeef9-113">On the **Product details** page:</span></span>

-   <span data-ttu-id="eeef9-114">Bir mağaza çalışanı farklı kanallardan gerçekleştirilen önceki hareketlere bakarken **Ürün ayrıntıları** sayfasını ziyaret ederse, öneri altyapısı birlikte satın alınabilecek ek maddeleri önerir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-114">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="eeef9-115">Mağaza çalışanı müşteriyi harekete ekler ve **Ürün ayrıntıları** sayfasını ziyaret ederse, öneri altyapısı müşteri hareket geçmişini kullanarak kişiselleştirilmiş öneriler sağlar.</span><span class="sxs-lookup"><span data-stu-id="eeef9-115">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="eeef9-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="eeef9-116">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="eeef9-117">**Hareket** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="eeef9-117">On the **Transaction** page:</span></span>

-   <span data-ttu-id="eeef9-118">Öneri altyapısı sepetteki maddelerin tam listesini temel olarak maddeler önerir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-118">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="eeef9-119">Mağaza çalışanı müşteriyi harekete eklerse, öneri altyapısı müşteri hareket geçmişini ve sepetteki maddelerin listesini kullanarak kişiselleştirilmiş öneriler sağlar.</span><span class="sxs-lookup"><span data-stu-id="eeef9-119">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="eeef9-120">**Hareket** sayfasında önerileri görüntülemek için, perakendecinin Dynamics 365 for Retail'da ekran düzenini güncelleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-120">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="eeef9-121">**Öneriler** denetimi, **Hareket** sayfasında atlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="eeef9-121">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="eeef9-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="eeef9-122">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="eeef9-123">**Müşteri ayrıntıları** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="eeef9-123">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="eeef9-124">Öneri altyapısı Kullanıcı kimliğini ve müşteri istek listesindeki maddeleri temel olarak maddeler önerir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-124">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="eeef9-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="eeef9-125">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="eeef9-126">Dynamics 365 for Retail'ı POS önerileri etkinleştirme işlemleri için yapılandırma</span><span class="sxs-lookup"><span data-stu-id="eeef9-126">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="eeef9-127">Ürün önerilerini ayarlamak için aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="eeef9-127">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="eeef9-128">Doğru **Tüzel kişilik** seçimi yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="eeef9-128">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="eeef9-129">**Varlık deposu**'na gidin, **Perakende satış**'ı seçin ve ardından **Yenile**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eeef9-129">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="eeef9-130">Bu, işlem veritabanınızdan alınan demo verileri (veya sizin verilerinizi) kullanır ve bunu Varlık deposuna taşır.</span><span class="sxs-lookup"><span data-stu-id="eeef9-130">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="eeef9-131">İsteğe bağlı: Hareket ekranında önerileri görüntülemek için **Ekran düzeni**'ne gidin ekran düzeninizi seçin, **Ekran düzeni tasarımcısı**'nı başlatın ve sonra **öneriler** denetimini gereken yere bırakın.</span><span class="sxs-lookup"><span data-stu-id="eeef9-131">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="eeef9-132">**Perakende parametreleri**'ne gidin, **Makine öğrenimi**'ni seçin, **POS önerilerini etkinleştir** altından **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="eeef9-132">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="eeef9-133">Önerileri POS'ta görmek için genel yapılandırma işini **1110** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="eeef9-133">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="eeef9-134">Yapılan değişiklikleri POS ekran düzeni tasarımcısına yansıtmak için, kanal yapılandırma işini **1070** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="eeef9-134">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="eeef9-135">[]()Nasıl çalışır?</span><span class="sxs-lookup"><span data-stu-id="eeef9-135">[]()How does it work?</span></span>
<span data-ttu-id="eeef9-136">**Varlık deposu** varlığını yenilediğinizde, aşağıdaki eylemleri gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-136">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="eeef9-137">Bilişsel hizmetler tarafından istenen biçimdeki veriler Dynamics 365 for Retail işlem veritabanından çıkarılır ve Varlık deposuna gönderilir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-137">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="eeef9-138">Veriler, Azure Data Factory (ADF) tarafından ADF etkinliklerinin bir parçası olarak Hive betiği kullanan verileri temizlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="eeef9-138">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="eeef9-139">Temizlenen veriler blob depolamada saklanır.</span><span class="sxs-lookup"><span data-stu-id="eeef9-139">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="eeef9-140">Blob depolamadaki veriler öneri modelini eğitmek amacıyla Bilişsel hizmetler API'sı tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="eeef9-140">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="eeef9-141">**Önerileri etkinleştir**'i açıp yapılandırma işlerini çalıştırdığınızda, aşağıdaki eylemler gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-141">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="eeef9-142">Model kimlik bilgileri ve kimliği API'dan toplanır ve Dynamics 365 for Retail işlem veritabanında, AOS için web.config'de ve ayrıca perakende sunucusunda depolanır.</span><span class="sxs-lookup"><span data-stu-id="eeef9-142">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="eeef9-143">Model kimlik bilgileri ve kimliği CRT'nin kullanımına sunulur, böylece Bulut POS ve MPOS'tan çevrimiçi modda gelen ürün önerileri çağrıları değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="eeef9-143">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="eeef9-144">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="eeef9-144">See also</span></span>
--------

[<span data-ttu-id="eeef9-145">POS cihazındaki hareket sayfasına öneriler denetimi ekleme</span><span class="sxs-lookup"><span data-stu-id="eeef9-145">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




