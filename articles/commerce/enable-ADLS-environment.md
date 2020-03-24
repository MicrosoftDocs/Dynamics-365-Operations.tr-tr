---
title: Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme
description: Bu konu, ürün önerilerinin etkinleştirilmesinin bir önkoşulu olan, Dynamics 365 Commerce ortamı için Azure Data Lake Storage'ın (ADSL) nasıl etkinleştirileceğini ve test edileceğini açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: 553e1512ba72559923403eef741ce08222172a09
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127779"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="b0cc0-103">Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b0cc0-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0cc0-104">Bu konu, ürün önerilerinin etkinleştirilmesinin bir önkoşulu olan, Dynamics 365 Commerce ortamı için Azure Data Lake Storage'ın (ADSL) nasıl etkinleştirileceğini ve test edileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="b0cc0-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="b0cc0-105">Overview</span></span>

<span data-ttu-id="b0cc0-106">Dynamics 365 Commerce çözümünde, tüm ürün ve hareket bilgileri ortamın Varlık deposunda izlenir.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="b0cc0-107">Bu verileri (veri analizi, iş zekası ve kişiselleştirilmiş öneriler gibi) diğer Dynamics 365 hizmetlerinin erişimine açmak için, ortamı, müşteriye ait bir Azure Data Lake Storage Gen 2 (ADLS) çözümüne bağlamak gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="b0cc0-108">ADLS bir ortamda yapılandırılırken, gerekli tüm veriler korunmaya devam eden ve müşterinin denetiminde bulunan Varlık deposundan yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="b0cc0-109">Ürün önerileri veya kişiselleştirilmiş öneriler de ortamda etkinleştirildiyse, müşteri verilerini almak ve bu verileri temel alan önerileri hesaplamak için, ürün önerileri yığınına ADLS içindeki özel klasöre erişim hakkı verilir.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b0cc0-110">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="b0cc0-110">Prerequisites</span></span>

<span data-ttu-id="b0cc0-111">Müşterilerin, sahip oldukları bir Azure aboneliğinde ADLS yapılandırmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="b0cc0-112">Bu konu bir Azure aboneliği satın almayı veya ADLS özelliği etkinleştirilmiş bir depolama hesabı kurulumunu kapsamaz.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="b0cc0-113">ADSL hakkında daha fazla bilgi için [ADSL resmi belgelerine](https://azure.microsoft.com/pricing/details/storage/data-lake) bakın.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="b0cc0-114">Yapılandırma adımları</span><span class="sxs-lookup"><span data-stu-id="b0cc0-114">Configuration steps</span></span>

<span data-ttu-id="b0cc0-115">Bu bölüm, bir ortamda ADLS etkinleştirmek için gereken yapılandırma adımlarını kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="b0cc0-116">Ortamda ADLS etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b0cc0-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="b0cc0-117">Ortamın arka ofis portalında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="b0cc0-118">**Sistem Parametreleri**ni arayın ve **Veri bağlantıları** sekmesine gidin.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="b0cc0-119">**Data Lake tümleştirmesi** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="b0cc0-120">**Data Lake'i yavaş yavaş güncelleştir** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="b0cc0-121">Sonra aşağıdaki gerekli bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="b0cc0-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="b0cc0-122">**Uygulama Kodu** // **Uygulama Parolası** // **DNS Adı** - ADLS gizliliğinin saklandığı KeyVault bağlanmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="b0cc0-123">**Parola adı** - KeyVault'ta depolanan ve ADLS ile kimlik doğrulamak için kullanılan parola adı.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="b0cc0-124">Değişikliklerinizi sayfanın sol üst köşesinde kaydedin.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="b0cc0-125">Aşağıdaki resimde örnek bir ADSL yapılandırması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-125">The following image shows an example ADLS configuration.</span></span>

![ADSL yapılandırması örneği](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="b0cc0-127">ADLS bağlantısını test etme</span><span class="sxs-lookup"><span data-stu-id="b0cc0-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="b0cc0-128">KeyVault'a bağlantıyı **Azure Key Vault'u test et** bağlantısını kullanarak test edin.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="b0cc0-129">ADSL'ye bağlantıyı **Azure Depolamayı test et** bağlantısını kullanarak test edin.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="b0cc0-130">Testler başarısız olursa, yukarıda eklenen tüm KeyVault bilgilerinin doğruluğunu iki kez kontrol edin ve sonra yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="b0cc0-131">Bağlantı testleri başarıyla sonuçlandıktan sonra Varlık deposu için otomatik yenilemeyi etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="b0cc0-132">Varlık deposu için otomatik yenilemeyi etkinleştirmek üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="b0cc0-133">**Varlık Deposu**'nu arayın.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="b0cc0-134">Soldaki listede **RetailSales** girişine gidin ve **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="b0cc0-135">**Otomatik Yenileme Etkin** ayarının **Evet** yapıldığından emin olun, **Yenile**'yi ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="b0cc0-136">Aşağıdaki resimde, otomatik yenilemenin etkinleştirildiği bir Varlık deposu örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Otomatik yenileme özelliği etkin olan Varlık deposu örneği](./media/exampleADLSConfig2.png)

<span data-ttu-id="b0cc0-138">Artık ADLS ortam için yapılandırılmış durumdadır.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="b0cc0-139">Henüz tamamlanmadıysa, ortam için [ürün önerilerini ve kişiselleştirmeyi etkinleştirme](enable-product-recommendations.md) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="b0cc0-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0cc0-140">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b0cc0-140">Additional resources</span></span>

[<span data-ttu-id="b0cc0-141">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="b0cc0-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b0cc0-142">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="b0cc0-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b0cc0-143">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b0cc0-143">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="b0cc0-144">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="b0cc0-144">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b0cc0-145">e-Ticaret sitesine önerisi listeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="b0cc0-145">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="b0cc0-146">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="b0cc0-146">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b0cc0-147">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="b0cc0-147">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b0cc0-148">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="b0cc0-148">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="b0cc0-149">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="b0cc0-149">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b0cc0-150">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="b0cc0-150">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="b0cc0-151">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="b0cc0-151">Product recommendations FAQ</span></span>](faq-recommendations.md)


