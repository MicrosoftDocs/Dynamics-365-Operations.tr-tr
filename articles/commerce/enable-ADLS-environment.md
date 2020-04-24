---
title: Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme
description: Bu konu, ürün önerilerinin etkinleştirilmesinin bir önkoşulu olan, Dynamics 365 Commerce ortamı için Azure Data Lake Storage'ın (ADSL) nasıl etkinleştirileceğini ve test edileceğini açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: ba428765babb9ca7566da7a457368959b1c29083
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259760"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="4cebe-103">Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4cebe-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4cebe-104">Bu konu, ürün önerilerinin etkinleştirilmesinin bir önkoşulu olan, Dynamics 365 Commerce ortamı için Azure Data Lake Storage'ın (ADSL) nasıl etkinleştirileceğini ve test edileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4cebe-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="4cebe-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="4cebe-105">Overview</span></span>

<span data-ttu-id="4cebe-106">Dynamics 365 Commerce çözümünde, tüm ürün ve hareket bilgileri ortamın Varlık deposunda izlenir.</span><span class="sxs-lookup"><span data-stu-id="4cebe-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="4cebe-107">Bu verileri (veri analizi, iş zekası ve kişiselleştirilmiş öneriler gibi) diğer Dynamics 365 hizmetlerinin erişimine açmak için, ortamı, müşteriye ait bir Azure Data Lake Storage Gen 2 (ADLS) çözümüne bağlamak gerekir.</span><span class="sxs-lookup"><span data-stu-id="4cebe-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="4cebe-108">ADLS bir ortamda yapılandırılırken, gerekli tüm veriler korunmaya devam eden ve müşterinin denetiminde bulunan Varlık deposundan yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="4cebe-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="4cebe-109">Ürün önerileri veya kişiselleştirilmiş öneriler de ortamda etkinleştirildiyse, müşteri verilerini almak ve bu verileri temel alan önerileri hesaplamak için, ürün önerileri yığınına ADLS içindeki özel klasöre erişim hakkı verilir.</span><span class="sxs-lookup"><span data-stu-id="4cebe-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4cebe-110">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="4cebe-110">Prerequisites</span></span>

<span data-ttu-id="4cebe-111">Müşterilerin, sahip oldukları bir Azure aboneliğinde ADLS yapılandırmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="4cebe-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="4cebe-112">Bu konu bir Azure aboneliği satın almayı veya ADLS özelliği etkinleştirilmiş bir depolama hesabı kurulumunu kapsamaz.</span><span class="sxs-lookup"><span data-stu-id="4cebe-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="4cebe-113">ADSL hakkında daha fazla bilgi için [ADSL resmi belgelerine](https://azure.microsoft.com/pricing/details/storage/data-lake) bakın.</span><span class="sxs-lookup"><span data-stu-id="4cebe-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="4cebe-114">Yapılandırma adımları</span><span class="sxs-lookup"><span data-stu-id="4cebe-114">Configuration steps</span></span>

<span data-ttu-id="4cebe-115">Bu bölüm, ürün önerileriyle ilgili bir ortamda ADLS öğesini etkinleştirmek için gerekli olan yapılandırma adımlarını kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4cebe-115">This section covers the configuration steps necessary for enabling ADLS in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="4cebe-116">ADLS'yi etkinleştirmek için gereken adımlara daha ayrıntılı bir genel bakış için bkz. [Veri deposununu Data Lake olarak kullanılabilir hale getirme](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="4cebe-116">For a more in-depth overview of the steps required to enable ADLS, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="4cebe-117">Ortamda ADLS etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4cebe-117">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="4cebe-118">Ortamın arka ofis portalında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="4cebe-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="4cebe-119">**Sistem Parametreleri**ni arayın ve **Veri bağlantıları** sekmesine gidin.</span><span class="sxs-lookup"><span data-stu-id="4cebe-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="4cebe-120">**Data Lake tümleştirmesi** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="4cebe-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="4cebe-121">**Data Lake'i yavaş yavaş güncelleştir** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="4cebe-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="4cebe-122">Sonra aşağıdaki gerekli bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="4cebe-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="4cebe-123">**Uygulama Kodu** // **Uygulama Parolası** // **DNS Adı** - ADLS gizliliğinin saklandığı KeyVault bağlanmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4cebe-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="4cebe-124">**Parola adı** - KeyVault'ta depolanan ve ADLS ile kimlik doğrulamak için kullanılan parola adı.</span><span class="sxs-lookup"><span data-stu-id="4cebe-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="4cebe-125">Değişikliklerinizi sayfanın sol üst köşesinde kaydedin.</span><span class="sxs-lookup"><span data-stu-id="4cebe-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="4cebe-126">Aşağıdaki resimde örnek bir ADSL yapılandırması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4cebe-126">The following image shows an example ADLS configuration.</span></span>

![ADSL yapılandırması örneği](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="4cebe-128">ADLS bağlantısını test etme</span><span class="sxs-lookup"><span data-stu-id="4cebe-128">Test the ADLS connection</span></span>

1. <span data-ttu-id="4cebe-129">KeyVault'a bağlantıyı **Azure Key Vault'u test et** bağlantısını kullanarak test edin.</span><span class="sxs-lookup"><span data-stu-id="4cebe-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="4cebe-130">ADSL'ye bağlantıyı **Azure Depolamayı test et** bağlantısını kullanarak test edin.</span><span class="sxs-lookup"><span data-stu-id="4cebe-130">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="4cebe-131">Testler başarısız olursa, yukarıda eklenen tüm KeyVault bilgilerinin doğruluğunu iki kez kontrol edin ve sonra yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="4cebe-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="4cebe-132">Bağlantı testleri başarıyla sonuçlandıktan sonra Varlık deposu için otomatik yenilemeyi etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4cebe-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="4cebe-133">Varlık deposu için otomatik yenilemeyi etkinleştirmek üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4cebe-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="4cebe-134">**Varlık Deposu**'nu arayın.</span><span class="sxs-lookup"><span data-stu-id="4cebe-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="4cebe-135">Soldaki listede **RetailSales** girişine gidin ve **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4cebe-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="4cebe-136">**Otomatik Yenileme Etkin** ayarının **Evet** yapıldığından emin olun, **Yenile**'yi ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4cebe-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="4cebe-137">Aşağıdaki resimde, otomatik yenilemenin etkinleştirildiği bir Varlık deposu örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4cebe-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Otomatik yenileme özelliği etkin olan Varlık deposu örneği](./media/exampleADLSConfig2.png)

<span data-ttu-id="4cebe-139">Artık ADLS ortam için yapılandırılmış durumdadır.</span><span class="sxs-lookup"><span data-stu-id="4cebe-139">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="4cebe-140">Henüz tamamlanmadıysa, ortam için [ürün önerilerini ve kişiselleştirmeyi etkinleştirme](enable-product-recommendations.md) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="4cebe-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4cebe-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4cebe-141">Additional resources</span></span>

[<span data-ttu-id="4cebe-142">Varlık deposunu Data Lake olarak kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="4cebe-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="4cebe-143">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="4cebe-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4cebe-144">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="4cebe-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="4cebe-145">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4cebe-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="4cebe-146">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="4cebe-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="4cebe-147">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="4cebe-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="4cebe-148">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="4cebe-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4cebe-149">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="4cebe-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="4cebe-150">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="4cebe-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="4cebe-151">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="4cebe-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="4cebe-152">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="4cebe-152">Product recommendations FAQ</span></span>](faq-recommendations.md)
