---
title: Ürün önerilerini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127894"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="98500-103">Ürün önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="98500-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="98500-104">Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="98500-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="98500-105">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="98500-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="98500-106">Öneriler ön kontrolü</span><span class="sxs-lookup"><span data-stu-id="98500-106">Recommendations pre-check</span></span>

<span data-ttu-id="98500-107">Etkinleştirmeden önce, lütfen, ürün önerilerinin, depolama alanını Azure Data Lake Storage (ADLS) kullanarak geçirmiş olan Commerce müşterileri için desteklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="98500-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="98500-108">ADLS'yi etkinleştirme adımları için bkz. [Bir Dynamics 365 ortamında ADLS nasıl etkinleştirilir?](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="98500-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="98500-109">Ek olarak, RetailSale ölçümlerinin etkinleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="98500-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="98500-110">Bu ayarla ilgili işlemi hakkında daha fazla bilgi edinmek için [buraya](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures) gidin.</span><span class="sxs-lookup"><span data-stu-id="98500-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="98500-111">Önerileri açın</span><span class="sxs-lookup"><span data-stu-id="98500-111">Turn on recommendations</span></span>

<span data-ttu-id="98500-112">Ürün önerilerini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="98500-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="98500-113">**Retail and Commerce &gt; Ürün önerileri &gt; Öneri parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="98500-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="98500-114">Paylaşılan parametreler listesinde, **Öneri Listeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="98500-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="98500-115">**Önerileri etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="98500-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Ürün önerilerini etkinleştirme](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="98500-117">Bu yordam, ürün öneri listeleri oluşturma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="98500-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="98500-118">Dynamics 365 Commerce'te listelerin kullanılabilmesi ve satış noktasında (POS) görülebilmesi için birkaç saate kadar gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="98500-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="98500-119">Öneri listesi parametrelerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="98500-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="98500-120">Varsayılan olarak, AI-ML tabanlı ürün öneri listesi önerilen değerleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="98500-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="98500-121">Varsayılan önerilen değerleri işinizin akışına uyacak şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98500-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="98500-122">Varsayılan parametrelerin nasıl değiştirileceği hakkında daha fazla bilgi edinmek için [AI-ML tabanlı ürün öneri sonuçlarınıYönet](modify-product-recommendation-results.md) bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="98500-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="98500-123">POS cihazlarındaki önerileri göster</span><span class="sxs-lookup"><span data-stu-id="98500-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="98500-124">Commerce arka ofisinde önerileri etkinleştirdikten sonra, öneriler panelinin düzenleme aracını kullanarak kontrol POS ekranına eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="98500-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="98500-125">Bu işlem hakkında bilgi edinmek için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="98500-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="98500-126">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="98500-126">Enable personalized recommendations</span></span>

<span data-ttu-id="98500-127">Kişiselleştirilmiş ürün önerilerinin nasıl alınacağı hakkında daha fazla bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="98500-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98500-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="98500-128">Additional resources</span></span>

[<span data-ttu-id="98500-129">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="98500-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="98500-130">Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="98500-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="98500-131">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="98500-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="98500-132">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="98500-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="98500-133">e-Ticaret sitesine önerisi listeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="98500-133">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="98500-134">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="98500-134">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="98500-135">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="98500-135">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="98500-136">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="98500-136">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="98500-137">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="98500-137">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="98500-138">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="98500-138">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="98500-139">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="98500-139">Product recommendations FAQ</span></span>](faq-recommendations.md)

