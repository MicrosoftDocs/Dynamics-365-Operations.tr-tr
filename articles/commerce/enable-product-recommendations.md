---
title: Ürün önerilerini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024968"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="ed5a1-103">Ürün önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ed5a1-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed5a1-104">Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="ed5a1-105">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="ed5a1-106">Öneriler ön kontrolü</span><span class="sxs-lookup"><span data-stu-id="ed5a1-106">Recommendations pre-check</span></span>

<span data-ttu-id="ed5a1-107">Etkinleştirmeden önce, lütfen, ürün önerilerinin, depolama alanını Azure Data Lake Storage (ADLS) kullanarak geçirmiş olan Commerce müşterileri için desteklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="ed5a1-108">ADLS'yi etkinleştirme adımları için bkz. [Bir Dynamics 365 ortamında ADLS nasıl etkinleştirilir?](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ed5a1-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="ed5a1-109">Ek olarak, RetailSale ölçümlerinin etkinleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="ed5a1-110">Bu ayarla ilgili işlemi hakkında daha fazla bilgi edinmek için [buraya](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures) gidin.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="ed5a1-111">Önerileri açın</span><span class="sxs-lookup"><span data-stu-id="ed5a1-111">Turn on recommendations</span></span>

<span data-ttu-id="ed5a1-112">Ürün önerilerini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="ed5a1-113">**Retail and Commerce &gt; Ürün önerileri &gt; Öneri parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="ed5a1-114">Paylaşılan parametreler listesinde, **Öneri Listeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="ed5a1-115">**Önerileri etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Ürün önerilerini etkinleştirme](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="ed5a1-117">Bu yordam, ürün öneri listeleri oluşturma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="ed5a1-118">Dynamics 365 Commerce'te listelerin kullanılabilmesi ve satış noktasında (POS) görülebilmesi için birkaç saate kadar gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="ed5a1-119">Öneri listesi parametrelerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="ed5a1-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="ed5a1-120">Varsayılan olarak, AI-ML tabanlı ürün öneri listesi önerilen değerleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="ed5a1-121">Varsayılan önerilen değerleri işinizin akışına uyacak şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="ed5a1-122">Varsayılan parametrelerin nasıl değiştirileceği hakkında daha fazla bilgi edinmek için [AI-ML tabanlı ürün öneri sonuçlarınıYönet](modify-product-recommendation-results.md) bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="ed5a1-123">POS cihazlarındaki önerileri göster</span><span class="sxs-lookup"><span data-stu-id="ed5a1-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="ed5a1-124">Commerce arka ofisinde önerileri etkinleştirdikten sonra, öneriler panelinin düzenleme aracını kullanarak kontrol POS ekranına eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ed5a1-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="ed5a1-125">Bu işlem hakkında bilgi edinmek için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="ed5a1-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="ed5a1-126">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ed5a1-126">Enable personalized recommendations</span></span>

<span data-ttu-id="ed5a1-127">Kişiselleştirilmiş ürün önerilerinin nasıl alınacağı hakkında daha fazla bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ed5a1-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed5a1-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ed5a1-128">Additional resources</span></span>

[<span data-ttu-id="ed5a1-129">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="ed5a1-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ed5a1-130">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ed5a1-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ed5a1-131">Sayfalarına ürün önerileri listesi ekleme</span><span class="sxs-lookup"><span data-stu-id="ed5a1-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="ed5a1-132">POS cihazlarına öneriler paneli Ekle</span><span class="sxs-lookup"><span data-stu-id="ed5a1-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ed5a1-133">Ürün topluluğu modülüne genel bakış</span><span class="sxs-lookup"><span data-stu-id="ed5a1-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="ed5a1-134">Dynamics 365 ortamında ADLS etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ed5a1-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

