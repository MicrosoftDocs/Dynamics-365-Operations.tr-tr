---
title: Ürün önerilerini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.
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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 694e5a451b8e25f3729364dfaed0adc7d242f2fe
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404221"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="5a72d-103">Ürün önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="5a72d-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a72d-104">Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5a72d-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="5a72d-105">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="5a72d-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="5a72d-106">Öneriler ön kontrolü</span><span class="sxs-lookup"><span data-stu-id="5a72d-106">Recommendations pre-check</span></span>

<span data-ttu-id="5a72d-107">Etkinleştirmeden önce ürün önerilerinin, depolama alanını Azure Data Lake Storage kullanarak geçirmiş olan Commerce müşterileri için desteklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5a72d-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="5a72d-108">Öneriler etkinleştirilmeden önce aşağıdaki yapılandırmalar arka ofiste etkinleştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="5a72d-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="5a72d-109">Azure Data Lake Storage'nin satın alındığından ve ortamda başarıyla doğrulandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="5a72d-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="5a72d-110">Daha fazla bilgi için bkz. [Azure Data Lake Storage'nin satın alındığından ve ortamda başarıyla doğrulandığından emin olma](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="5a72d-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="5a72d-111">Varlık deposu yenilemenin otomatik olarak yapıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="5a72d-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="5a72d-112">Daha fazla bilgi için bkz. [Varlık deposu yenilemesinin otomatik yapıldığından emin olun](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="5a72d-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="5a72d-113">Azure AD Kimlik yapılandırmasının Öneriler için bir giriş içerdiğini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="5a72d-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="5a72d-114">Bu eylemin nasıl yapılacağı ile ilgili daha fazla bilgi aşağıda verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5a72d-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="5a72d-115">Ek olarak, RetailSale ölçümlerinin etkinleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="5a72d-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="5a72d-116">Bu ayar işlemi hakkında daha fazla bilgi edinmek için bkz. [Ölçümlerle çalışma](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="5a72d-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="5a72d-117">Azure AD Kimlik yapılandırması</span><span class="sxs-lookup"><span data-stu-id="5a72d-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="5a72d-118">Bu adım, Hizmet olarak alt yapı (IaaS) yapılandırması çalıştıran tüm müşteriler için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5a72d-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="5a72d-119">Service Fabric (SF) üzerinde çalışan müşteriler için bu adım otomatik olmalıdır ve ayarın beklendiği şekilde yapılandırıldığını doğrulamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="5a72d-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="5a72d-120">Ayar</span><span class="sxs-lookup"><span data-stu-id="5a72d-120">Setup</span></span>

1. <span data-ttu-id="5a72d-121">Arka ofisten, **Azure Active Directory uygulamaları** sayfasını arayın.</span><span class="sxs-lookup"><span data-stu-id="5a72d-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="5a72d-122">"RecommendationSystemApplication-1" için bir giriş olup olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="5a72d-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="5a72d-123">Giriş yoksa, aşağıdaki bilgilerle yeni bir giriş ekleyin:</span><span class="sxs-lookup"><span data-stu-id="5a72d-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="5a72d-124">**İstemcı Kodu** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="5a72d-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="5a72d-125">**Ad** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="5a72d-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="5a72d-126">**Kullanıcı Kimliği** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="5a72d-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="5a72d-127">Sayfayı kaydet ve kapatın</span><span class="sxs-lookup"><span data-stu-id="5a72d-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="5a72d-128">Önerileri açın</span><span class="sxs-lookup"><span data-stu-id="5a72d-128">Turn on recommendations</span></span>

<span data-ttu-id="5a72d-129">Ürün önerilerini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5a72d-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="5a72d-130">**Retail and Commerce &gt; Ürün önerileri &gt; Öneri parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5a72d-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="5a72d-131">Paylaşılan parametreler listesinde, **Öneri Listeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5a72d-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="5a72d-132">**Önerileri etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5a72d-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![Önerileri açma](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="5a72d-134">Bu yordam, ürün öneri listeleri oluşturma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="5a72d-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="5a72d-135">Dynamics 365 Commerce'ta veya satış noktasında (POS) listelerin kullanılabilmesi ve görüntülenmesi için birkaç saat gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="5a72d-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="5a72d-136">Öneri listesi parametrelerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="5a72d-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="5a72d-137">Varsayılan olarak, AI-ML tabanlı ürün öneri listesi önerilen değerleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="5a72d-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="5a72d-138">Varsayılan önerilen değerleri işinizin akışına uyacak şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a72d-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="5a72d-139">Varsayılan parametrelerin nasıl değiştirileceği hakkında daha fazla bilgi edinmek için [AI-ML tabanlı ürün öneri sonuçlarınıYönet](modify-product-recommendation-results.md) bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="5a72d-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="5a72d-140">POS cihazlarındaki önerileri göster</span><span class="sxs-lookup"><span data-stu-id="5a72d-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="5a72d-141">Commerce arka ofisinde önerileri etkinleştirdikten sonra, öneriler panelinin düzenleme aracını kullanarak kontrol POS ekranına eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5a72d-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="5a72d-142">Bu işlem hakkında bilgi edinmek için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="5a72d-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="5a72d-143">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="5a72d-143">Enable personalized recommendations</span></span>

<span data-ttu-id="5a72d-144">Dynamics 365 Commerce uygulamasında perakendeciler, kişiselleştirilmiş ürün önerileri (kişiselleştirme olarak da bilinir) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5a72d-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="5a72d-145">Böylece, kişiselleştirilmiş öneriler müşteri deneyimine çevrimiçi ve satış noktasında dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="5a72d-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="5a72d-146">Kişiselleştirme işlevi açıldığında, sistem, bir kullanıcının satın alma ve ürün bilgilerini, kişiselleştirilmemiş ürün önerileri oluşturmak üzere ilişkilendirebilir.</span><span class="sxs-lookup"><span data-stu-id="5a72d-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="5a72d-147">Kişiselleştirilmiş ürün önerileri hakkında daha fazla bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="5a72d-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a72d-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5a72d-148">Additional resources</span></span>

[<span data-ttu-id="5a72d-149">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="5a72d-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="5a72d-150">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="5a72d-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="5a72d-151">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="5a72d-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="5a72d-152">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="5a72d-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="5a72d-153">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="5a72d-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="5a72d-154">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="5a72d-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="5a72d-155">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="5a72d-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="5a72d-156">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a72d-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="5a72d-157">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a72d-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="5a72d-158">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="5a72d-158">Product recommendations FAQ</span></span>](faq-recommendations.md)

