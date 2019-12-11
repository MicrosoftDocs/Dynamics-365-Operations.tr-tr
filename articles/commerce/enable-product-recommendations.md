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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770151"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="47780-103">Ürün önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="47780-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="47780-104">Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="47780-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="47780-105">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="47780-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="47780-106">Öneriler ön kontrolü</span><span class="sxs-lookup"><span data-stu-id="47780-106">Recommendations pre-check</span></span>
<span data-ttu-id="47780-107">Etkinleştirmeden önce, lütfen ürün önerilerinin yapı 10.0.6 destekleyen ve depolama alanını BDL'yi kullanarak geçirmiş olan F&O müşterileri için desteklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="47780-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="47780-108">Ek olarak, RetailSale ölçümlerinin etkinleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="47780-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="47780-109">Bu ayarla ilgili işlemi hakkında daha fazla bilgi edinmek için [buraya](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures) gidin.</span><span class="sxs-lookup"><span data-stu-id="47780-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="47780-110">Önerileri açın</span><span class="sxs-lookup"><span data-stu-id="47780-110">Turn on recommendations</span></span>

<span data-ttu-id="47780-111">Ürün önerilerini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="47780-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="47780-112">**Perakende** &gt; **ürün önerileri** &gt; **öneri parametrelerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="47780-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="47780-113">Perakende paylaşılan parametreleri listesinde, **öneri listelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="47780-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="47780-114">**Önerileri etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="47780-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![Ürün önerilerini etkinleştirme](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="47780-116">Bu yordam, ürün öneri listeleri oluşturma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="47780-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="47780-117">Dynamics 365 for Commerce'te listelerin kullanılabilmesi ve satış noktasında (POS) görülebilmesi için birkaç saate kadar gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="47780-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="47780-118">Öneri listesi parametrelerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="47780-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="47780-119">Varsayılan olarak, AI-ML tabanlı ürün öneri listesi önerilen değerleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="47780-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="47780-120">Varsayılan önerilen değerleri işinizin akışına uyacak şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47780-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="47780-121">Varsayılan parametrelerin nasıl değiştirileceği hakkında daha fazla bilgi edinmek için [AI-ML tabanlı ürün öneri sonuçlarınıYönet](modify-product-recommendation-results.md) bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="47780-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="47780-122">POS cihazlarındaki önerileri göster</span><span class="sxs-lookup"><span data-stu-id="47780-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="47780-123">Arka ofisin önerilerini etkinleştirdikten sonra, öneriler panelinin düzenleme aracı ile kontrol POS ekranına eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="47780-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="47780-124">Bu ayarla ilgili işlemi hakkında daha fazla bilgi edinmek için [buraya](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) gidin.</span><span class="sxs-lookup"><span data-stu-id="47780-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="47780-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="47780-125">Additional resources</span></span>

[<span data-ttu-id="47780-126">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="47780-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="47780-127">Sayfalarına ürün önerileri listesi ekleme</span><span class="sxs-lookup"><span data-stu-id="47780-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="47780-128">POS cihazlarına öneriler paneli Ekle</span><span class="sxs-lookup"><span data-stu-id="47780-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


