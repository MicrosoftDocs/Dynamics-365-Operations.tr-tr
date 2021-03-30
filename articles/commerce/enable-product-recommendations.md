---
title: Ürün önerilerini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcb3b542d290e01a3cddc73ae163ed2ef420771b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238809"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="37b8a-103">Ürün önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="37b8a-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="37b8a-104">Bu konu, Microsoft Dynamics 365 Commerce müşterileri için yapay bilgi destek sistemi öğrenme (AI-ML) tabanlı ürün önerilerinin nasıl yapılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="37b8a-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="37b8a-105">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="37b8a-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="37b8a-106">Öneriler ön kontrolü</span><span class="sxs-lookup"><span data-stu-id="37b8a-106">Recommendations pre-check</span></span>

<span data-ttu-id="37b8a-107">Etkinleştirmeden önce ürün önerilerinin, depolama alanını Azure Data Lake Storage kullanarak geçirmiş olan Commerce müşterileri için desteklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="37b8a-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="37b8a-108">Öneriler etkinleştirilmeden önce aşağıdaki yapılandırmalar arka ofiste etkinleştirilmelidir:</span><span class="sxs-lookup"><span data-stu-id="37b8a-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="37b8a-109">Azure Data Lake Storage'nin satın alındığından ve ortamda başarıyla doğrulandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="37b8a-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="37b8a-110">Daha fazla bilgi için bkz. [Azure Data Lake Storage'nin satın alındığından ve ortamda başarıyla doğrulandığından emin olma](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="37b8a-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="37b8a-111">Varlık deposu yenilemenin otomatik olarak yapıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="37b8a-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="37b8a-112">Daha fazla bilgi için bkz. [Varlık deposu yenilemesinin otomatik yapıldığından emin olun](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="37b8a-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="37b8a-113">Azure AD Kimlik yapılandırmasının Öneriler için bir giriş içerdiğini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="37b8a-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="37b8a-114">Bu eylemin nasıl yapılacağı ile ilgili daha fazla bilgi aşağıda verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="37b8a-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="37b8a-115">Ek olarak, RetailSale ölçümlerinin etkinleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="37b8a-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="37b8a-116">Bu ayar işlemi hakkında daha fazla bilgi edinmek için bkz. [Ölçümlerle çalışma](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="37b8a-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="37b8a-117">Azure AD Kimlik yapılandırması</span><span class="sxs-lookup"><span data-stu-id="37b8a-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="37b8a-118">Bu adım, Hizmet olarak alt yapı (IaaS) yapılandırması çalıştıran tüm müşteriler için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="37b8a-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="37b8a-119">Service Fabric (SF) üzerinde çalışan müşteriler için bu adım otomatik olmalıdır ve ayarın beklendiği şekilde yapılandırıldığını doğrulamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="37b8a-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="37b8a-120">Ayar</span><span class="sxs-lookup"><span data-stu-id="37b8a-120">Setup</span></span>

1. <span data-ttu-id="37b8a-121">Arka ofisten, **Azure Active Directory uygulamaları** sayfasını arayın.</span><span class="sxs-lookup"><span data-stu-id="37b8a-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="37b8a-122">"RecommendationSystemApplication-1" için bir giriş olup olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="37b8a-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="37b8a-123">Giriş yoksa, aşağıdaki bilgilerle yeni bir giriş ekleyin:</span><span class="sxs-lookup"><span data-stu-id="37b8a-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="37b8a-124">**İstemcı Kodu** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="37b8a-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="37b8a-125">**Ad** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="37b8a-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="37b8a-126">**Kullanıcı Kimliği** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="37b8a-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="37b8a-127">Sayfayı kaydet ve kapatın</span><span class="sxs-lookup"><span data-stu-id="37b8a-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="37b8a-128">Önerileri açın</span><span class="sxs-lookup"><span data-stu-id="37b8a-128">Turn on recommendations</span></span>

<span data-ttu-id="37b8a-129">Ürün önerilerini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="37b8a-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="37b8a-130">Commerce Headquarters'ta **Özellik Yönetimi**'ni arayın.</span><span class="sxs-lookup"><span data-stu-id="37b8a-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="37b8a-131">Kullanılabilir özelliklerin listesini görmek için **Tümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="37b8a-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="37b8a-132">Arama kutusuna **Öneriler** yazın.</span><span class="sxs-lookup"><span data-stu-id="37b8a-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="37b8a-133">**Ürün önerileri** özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="37b8a-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="37b8a-134">**Ürün önerileri** özellikler bölmesinde **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="37b8a-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Önerileri açma](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="37b8a-136">Bu yordam, ürün öneri listeleri oluşturma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="37b8a-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="37b8a-137">Dynamics 365 Commerce'ta veya satış noktasında (POS) listelerin kullanılabilmesi ve görüntülenmesi için birkaç saat gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="37b8a-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="37b8a-138">Öneri listesi parametrelerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="37b8a-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="37b8a-139">Varsayılan olarak, AI-ML tabanlı ürün öneri listesi önerilen değerleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="37b8a-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="37b8a-140">Varsayılan önerilen değerleri işinizin akışına uyacak şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37b8a-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="37b8a-141">Varsayılan parametrelerin nasıl değiştirileceği hakkında daha fazla bilgi edinmek için [AI-ML tabanlı ürün öneri sonuçlarınıYönet](modify-product-recommendation-results.md) bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="37b8a-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="37b8a-142">POS cihazlarındaki önerileri göster</span><span class="sxs-lookup"><span data-stu-id="37b8a-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="37b8a-143">Commerce arka ofisinde önerileri etkinleştirdikten sonra, öneriler panelinin düzenleme aracını kullanarak kontrol POS ekranına eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="37b8a-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="37b8a-144">Bu işlem hakkında bilgi edinmek için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="37b8a-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="37b8a-145">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="37b8a-145">Enable personalized recommendations</span></span>

<span data-ttu-id="37b8a-146">Dynamics 365 Commerce uygulamasında perakendeciler, kişiselleştirilmiş ürün önerileri (kişiselleştirme olarak da bilinir) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="37b8a-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="37b8a-147">Böylece, kişiselleştirilmiş öneriler müşteri deneyimine çevrimiçi ve satış noktasında dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="37b8a-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="37b8a-148">Kişiselleştirme işlevi açıldığında, sistem, bir kullanıcının satın alma ve ürün bilgilerini, kişiselleştirilmemiş ürün önerileri oluşturmak üzere ilişkilendirebilir.</span><span class="sxs-lookup"><span data-stu-id="37b8a-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="37b8a-149">Kişiselleştirilmiş ürün önerileri hakkında daha fazla bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="37b8a-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37b8a-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="37b8a-150">Additional resources</span></span>

[<span data-ttu-id="37b8a-151">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="37b8a-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="37b8a-152">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="37b8a-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="37b8a-153">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="37b8a-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="37b8a-154">"Benzer görünümleri araştır" önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="37b8a-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="37b8a-155">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="37b8a-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="37b8a-156">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="37b8a-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="37b8a-157">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="37b8a-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="37b8a-158">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="37b8a-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="37b8a-159">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="37b8a-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="37b8a-160">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="37b8a-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="37b8a-161">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="37b8a-161">Product recommendations FAQ</span></span>](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]