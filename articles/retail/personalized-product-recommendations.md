---
title: "Kişiselleştirilmiş ürün önerileri"
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 368468a1c1cd023862f1405dddf3a90574edce22
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="personalized-product-recommendations"></a><span data-ttu-id="7d577-103">Kişiselleştirilmiş ürün önerileri</span><span class="sxs-lookup"><span data-stu-id="7d577-103">Personalized product recommendations</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="7d577-104">Bu özelliği daha iyi bir algoritma ve daha yeni perakende odaklı yeteneklerle yeniden tasarladığımızdan ürün öneri hizmetinin geçerli sürümünü kaldırıyoruz.</span><span class="sxs-lookup"><span data-stu-id="7d577-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="7d577-105">Daha fazla bilgi için bkz. [Kaldırılan veya artık kullanılmayan özellikler](../dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="7d577-105">For more information see [Removed or deprecated features](../dev-itpro/migration-upgrade/deprecated-features.md).</span></span> <span data-ttu-id="7d577-106">Ortamınız için zaten etkin ürün önerileri ile ilgili sorunlarla karşılaşırsanız sayfanın alt kısmına gidin.</span><span class="sxs-lookup"><span data-stu-id="7d577-106">Navigate to the bottom of the page if you are facing issues with already-enabled product recommendations for your environment.</span></span> 

<span data-ttu-id="7d577-107">Dynamics 365 for Retail'da, ürün önerileri satış noktası cihazında (POS) görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="7d577-107">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="7d577-108">Öneriler satınalma geçmişi, istek listelerindeki maddeler ve diğer müşterilerin çevrimiçi ve fiziksel mağazalardan aldıkları maddelere dayanarak müşterilerin ilgi duyabilecekleri maddelerdir.</span><span class="sxs-lookup"><span data-stu-id="7d577-108">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="7d577-109">Büyük kataloglara sahip perakendeciler için öneriler müşterinin ürün bulmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="7d577-109">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="7d577-110">Müşterinin ilgi alanlarını ve satın alma alışkanlıklarını hedefleyen ürünleri sunarak , ürün önerileri perakendecilere çapraz satış ve yukarı satış konusunda yardımı olabilir ve müşteri tutmayı geliştirebilir.</span><span class="sxs-lookup"><span data-stu-id="7d577-110">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="7d577-111">Dynamics 365 for Retail'de ürün önerileri bilişsel hizmetler ve Microsoft Azure makine öğrenimiyle desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7d577-111">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="7d577-112">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="7d577-112">Scenarios</span></span>
---------

<span data-ttu-id="7d577-113">Ürün önerileri aşağıdaki POS senaryoları için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7d577-113">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="7d577-114">Bulut POS veya Modern POS'da (MPOS) kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7d577-114">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="7d577-115">**Ürün ayrıntıları** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="7d577-115">On the **Product details** page:</span></span>

-   <span data-ttu-id="7d577-116">Bir mağaza çalışanı farklı kanallardan gerçekleştirilen önceki hareketlere bakarken **Ürün ayrıntıları** sayfasını ziyaret ederse, öneri altyapısı birlikte satın alınabilecek ek maddeleri önerir.</span><span class="sxs-lookup"><span data-stu-id="7d577-116">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="7d577-117">Mağaza çalışanı müşteriyi harekete ekler ve **Ürün ayrıntıları** sayfasını ziyaret ederse, öneri altyapısı müşteri hareket geçmişini kullanarak kişiselleştirilmiş öneriler sağlar.</span><span class="sxs-lookup"><span data-stu-id="7d577-117">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="7d577-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="7d577-118">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="7d577-119">**Hareket** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="7d577-119">On the **Transaction** page:</span></span>

-   <span data-ttu-id="7d577-120">Öneri altyapısı sepetteki maddelerin tam listesini temel olarak maddeler önerir.</span><span class="sxs-lookup"><span data-stu-id="7d577-120">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="7d577-121">Mağaza çalışanı müşteriyi harekete eklerse, öneri altyapısı müşteri hareket geçmişini ve sepetteki maddelerin listesini kullanarak kişiselleştirilmiş öneriler sağlar.</span><span class="sxs-lookup"><span data-stu-id="7d577-121">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="7d577-122">**Hareket** sayfasında önerileri görüntülemek için, perakendecinin Dynamics 365 for Retail'da ekran düzenini güncelleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7d577-122">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="7d577-123">**Öneriler** denetimi, **Hareket** sayfasında atlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7d577-123">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="7d577-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="7d577-124">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="7d577-125">**Müşteri ayrıntıları** sayfasında:</span><span class="sxs-lookup"><span data-stu-id="7d577-125">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="7d577-126">Öneri altyapısı Kullanıcı kimliğini ve müşteri istek listesindeki maddeleri temel olarak maddeler önerir.</span><span class="sxs-lookup"><span data-stu-id="7d577-126">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="7d577-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="7d577-127">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="7d577-128">Dynamics 365 for Retail'ı POS önerileri etkinleştirme işlemleri için yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7d577-128">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="7d577-129">Ürün önerilerini ayarlamak için aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="7d577-129">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="7d577-130">Doğru **Tüzel kişilik** seçimi yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7d577-130">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="7d577-131">**Varlık deposu**'na gidin, **Perakende satış**'ı seçin ve ardından **Yenile**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d577-131">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="7d577-132">Bu, işlem veritabanınızdan alınan demo verileri (veya sizin verilerinizi) kullanır ve bunu Varlık deposuna taşır.</span><span class="sxs-lookup"><span data-stu-id="7d577-132">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="7d577-133">İsteğe bağlı: Hareket ekranında önerileri görüntülemek için **Ekran düzeni**'ne gidin ekran düzeninizi seçin, **Ekran düzeni tasarımcısı**'nı başlatın ve sonra **öneriler** denetimini gereken yere bırakın.</span><span class="sxs-lookup"><span data-stu-id="7d577-133">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="7d577-134">**Perakende parametreleri**'ne gidin, **Makine öğrenimi**'ni seçin, **POS önerilerini etkinleştir** altından **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="7d577-134">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="7d577-135">Önerileri POS'ta görmek için genel yapılandırma işini **1110** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7d577-135">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="7d577-136">Yapılan değişiklikleri POS ekran düzeni tasarımcısına yansıtmak için, kanal yapılandırma işini **1070** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7d577-136">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="7d577-137">Nasıl çalışır?</span><span class="sxs-lookup"><span data-stu-id="7d577-137">How does it work?</span></span>
<span data-ttu-id="7d577-138">**Varlık deposu** varlığını yenilediğinizde, aşağıdaki eylemleri gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="7d577-138">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="7d577-139">Bilişsel hizmetler tarafından istenen biçimdeki veriler Dynamics 365 for Retail işlem veritabanından çıkarılır ve Varlık deposuna gönderilir.</span><span class="sxs-lookup"><span data-stu-id="7d577-139">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="7d577-140">Veriler, Azure Data Factory (ADF) tarafından ADF etkinliklerinin bir parçası olarak Hive betiği kullanan verileri temizlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7d577-140">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="7d577-141">Temizlenen veriler blob depolamada saklanır.</span><span class="sxs-lookup"><span data-stu-id="7d577-141">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="7d577-142">Blob depolamadaki veriler öneri modelini eğitmek amacıyla Bilişsel hizmetler API'sı tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7d577-142">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="7d577-143">**Önerileri etkinleştir**'i açıp yapılandırma işlerini çalıştırdığınızda, aşağıdaki eylemler gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="7d577-143">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="7d577-144">Model kimlik bilgileri ve kimliği API'dan toplanır ve Dynamics 365 for Retail işlem veritabanında, AOS için web.config'de ve ayrıca perakende sunucusunda depolanır.</span><span class="sxs-lookup"><span data-stu-id="7d577-144">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="7d577-145">Model kimlik bilgileri ve kimliği CRT'nin kullanımına sunulur, böylece Bulut POS ve MPOS'tan çevrimiçi modda gelen ürün önerileri çağrıları değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="7d577-145">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>

> ## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="7d577-146">Zaten etkinleştirilmiş ürün önerileriyle ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="7d577-146">Troubleshoot issues where you have Product recommendations already enabled</span></span> 
> - <span data-ttu-id="7d577-147">**Perakende Parametreleri** > **Makine öğrenimi** > **Ürün önerilerini devre dışı bırak**'a gidin ve **Ürün yapılandırma işini [1110]** çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7d577-147">Navigate to **Retail Parameters** > **Machine learning** > **Disable product recommendations** and run **Global configuration job [1110]**.</span></span> <span data-ttu-id="7d577-148">**Makine öğrenimi** sekmesini bulamıyorsanız, lütfen Dynamics Destek birimine başvurun.</span><span class="sxs-lookup"><span data-stu-id="7d577-148">If you are not able to locate **Machine learning** tab, please contact Dynamics Support.</span></span> 
> 
> - <span data-ttu-id="7d577-149">**Öneriler denetimini** hareket ekranınıza **Ekran düzeni tasarımcısını** kullanarak eklediyseniz bunu da kaldırın.</span><span class="sxs-lookup"><span data-stu-id="7d577-149">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span> 



<a name="additional-resources"></a><span data-ttu-id="7d577-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7d577-150">Additional resources</span></span>
--------

[<span data-ttu-id="7d577-151">POS cihazındaki hareket sayfasına öneriler denetimi ekleme</span><span class="sxs-lookup"><span data-stu-id="7d577-151">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




