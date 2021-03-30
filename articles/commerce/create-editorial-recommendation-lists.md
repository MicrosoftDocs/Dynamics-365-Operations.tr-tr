---
title: Seçkin önerileri el ile oluşturma
description: Bu konu, tacirlerin Microsoft Dynamics 365 Commerce müşterileri için el ile ürün listeleri oluşturma ve yönetme yöntemini açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7dd9de055a020d7171aa2dea45714933b0987d49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208000"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="31c6b-103">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="31c6b-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="31c6b-104">Bu konu, tacirlerin Microsoft Dynamics 365 Commerce müşterileri için el ile ürün önerileri listeleri oluşturma ve yönetme yöntemini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="31c6b-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="31c6b-105">Seçkin listeler, kişiler tarafından oluşturulan ve seçkin bağımsız içerik koleksiyonlarıdır.</span><span class="sxs-lookup"><span data-stu-id="31c6b-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="31c6b-106">Yeni liste oluşturun.</span><span class="sxs-lookup"><span data-stu-id="31c6b-106">Create a new list</span></span>

<span data-ttu-id="31c6b-107">Seçkin bir ürün önerisi listesi oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="31c6b-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="31c6b-108">**Retail and Commerce &gt; Ürün önerileri &gt; Öneri listeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="31c6b-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="31c6b-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="31c6b-109">Select **New**.</span></span>
1. <span data-ttu-id="31c6b-110">**Liste kimliği** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="31c6b-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="31c6b-111">**Liste adı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="31c6b-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="31c6b-112">**Liste adı**, **ürün toplama** modülünün seçkin listeler bölümünde görünecek listenin başlığı.</span><span class="sxs-lookup"><span data-stu-id="31c6b-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="31c6b-113">Listeye ürün eklemek için **Ürün ekle** seçin.</span><span class="sxs-lookup"><span data-stu-id="31c6b-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="31c6b-114">Listedeki ürünlerin sırasını değiştirmek için **görüntüleme sırası** sütununa bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="31c6b-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="31c6b-115">İki ürün aynı görüntü sipariş değerine sahipse, bu iki sonucun son sırası arka ofisten farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="31c6b-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="31c6b-116">Listeyi kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="31c6b-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="31c6b-117">Örnek Listesi</span><span class="sxs-lookup"><span data-stu-id="31c6b-117">Example List</span></span>

![Arka ofis içindeki örnek seçkin liste](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="31c6b-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="31c6b-119">Additional resources</span></span>

[<span data-ttu-id="31c6b-120">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="31c6b-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="31c6b-121">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="31c6b-121">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="31c6b-122">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="31c6b-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="31c6b-123">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="31c6b-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="31c6b-124">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="31c6b-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="31c6b-125">"Benzer görünümleri araştır" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="31c6b-125">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="31c6b-126">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="31c6b-126">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="31c6b-127">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="31c6b-127">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="31c6b-128">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="31c6b-128">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="31c6b-129">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="31c6b-129">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="31c6b-130">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="31c6b-130">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]