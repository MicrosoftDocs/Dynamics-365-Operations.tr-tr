---
title: Demo verileriyle öneriler oluşturma
description: Bu konuda, önceden doldurulan ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.
author: bebeale
manager: AnnBe
ms.date: 05/26/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 68275f3e36bce0f641b0273cf3b3b8c8ce9db137
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404337"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="ead28-103">Demo verileriyle öneriler oluşturma</span><span class="sxs-lookup"><span data-stu-id="ead28-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ead28-104">Bu konuda, önceden doldurulan ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ead28-104">This topic provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="ead28-105">Çoklu kanal ürün önerilerinde, editör tarafından düzenlenen veya program tarafından oluşturulan bir dizi sipariş edilmiş ürünlerin listesini sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ead28-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="ead28-106">Bu listeler, iş ihtiyaçlarınıza bağlı olarak birçok senaryoda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ead28-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="ead28-107">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="ead28-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="ead28-108">Katman 2 ve daha yüksek Dynamics 365 Ortamlarında ürün önerileri, müşteri verilerine göre otomatik olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="ead28-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="ead28-109">Ürün önerileri tanıtım verilerini kullanmak, ortamda zaten sağlanmış olan herhangi bir ürün önerisi çözümünü ve bu çözümün kullanımıyla ilişkili hiçbir maliyeti devre dışı bırakmaz.</span><span class="sxs-lookup"><span data-stu-id="ead28-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="ead28-110">Katman 1 ortamlarında ürün önerilerinde yalnızca .csv dosyasında depolanan statik tanıtım verileri esas alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ead28-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="ead28-111">Bir ortamdaki ürün önerileri tanıtım verilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ead28-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="ead28-112">Ürün örnerileri demo tarhini etkinleştirmek için Müşterilerin Dynamics 365 Commerce Önizleme Tanıtım Uzantısı'nı ilgili ortama dağıtması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ead28-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="ead28-113">Böylece, ürün önerileri tanıtım verileri otomatik olarak etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ead28-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="ead28-114">Varsayılan tanıtım verileri</span><span class="sxs-lookup"><span data-stu-id="ead28-114">Default demo data</span></span>
<span data-ttu-id="ead28-115">Her OneBox türü ortamı, virgülle ayrılan Commerce Scale Unit'da bulunan ‘reco_demo_data.csv’ dosyasında depolanan bir dizi önceden yüklenmiş ürün önerileriyle birlikte gelir.</span><span class="sxs-lookup"><span data-stu-id="ead28-115">Each OneBox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="ead28-116">Bu veriler, aşağıdaki sütunlar boyunca yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="ead28-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="ead28-117">Sütun adı</span><span class="sxs-lookup"><span data-stu-id="ead28-117">Column name</span></span>         | <span data-ttu-id="ead28-118">Zorunlu</span><span class="sxs-lookup"><span data-stu-id="ead28-118">Mandatory</span></span>          | <span data-ttu-id="ead28-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="ead28-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="ead28-120">Olası değerler</span><span class="sxs-lookup"><span data-stu-id="ead28-120">Possible values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ead28-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="ead28-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="ead28-123">Tanıtım veri noktasının oluşturulması gereken özel ürün önerisi listesi türü.</span><span class="sxs-lookup"><span data-stu-id="ead28-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="ead28-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="ead28-124">RecoBestSelling</span></span></li><li><span data-ttu-id="ead28-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="ead28-125">RecoNew</span></span></li><li><span data-ttu-id="ead28-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="ead28-126">RecoTrending</span></span></li><li><span data-ttu-id="ead28-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="ead28-127">RecoCart</span></span></li><li><span data-ttu-id="ead28-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="ead28-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="ead28-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="ead28-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="ead28-131">Ürün önerilerinin kullanıma sunulmasının beklendiği özel işletme birimi numarası.</span><span class="sxs-lookup"><span data-stu-id="ead28-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="ead28-132">Kategori</span><span class="sxs-lookup"><span data-stu-id="ead28-132">Category</span></span>            |                    |    <span data-ttu-id="ead28-133">Özel listenin geri döndürülmesi gerektiği kategori.</span><span class="sxs-lookup"><span data-stu-id="ead28-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="ead28-134">Hiçbir kategori belirtilmezse liste, yalnızca gezinti hiyerarşisinin üst kısmı içindir.</span><span class="sxs-lookup"><span data-stu-id="ead28-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="ead28-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="ead28-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="ead28-136">Çekirdek ürünün olması gerektiği listelerde (RecoPeopleAlsoBuy and RecoCart) ek ürünler gösterilmelidir.</span><span class="sxs-lookup"><span data-stu-id="ead28-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="ead28-137">CustomerId</span><span class="sxs-lookup"><span data-stu-id="ead28-137">CustomerId</span></span>          |                    |    <span data-ttu-id="ead28-138">Müşteri tanımlayıcısı gerektiren listeler için (RecoPicks).</span><span class="sxs-lookup"><span data-stu-id="ead28-138">For lists that require a customer identifier (RecoPicks).</span></span>  <span data-ttu-id="ead28-139">Varsayılan '0' değeri tüm müşteriler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="ead28-139">The default value '0' applies to all customers.</span></span>          |                                                                              |
| <span data-ttu-id="ead28-140">ItemIds</span><span class="sxs-lookup"><span data-stu-id="ead28-140">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="ead28-142">Sonuç olarak döndürülmesi gereken ve ‘;’ ile ayrılan bir veya daha fazla ürün.</span><span class="sxs-lookup"><span data-stu-id="ead28-142">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="ead28-143">Tanıtım verilerini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="ead28-143">Customize demo data</span></span>
<span data-ttu-id="ead28-144">HQ'da yapılandırılan tüm ürün ve kategori bilgileriyle varsayılan tanıtım verilerini düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ead28-144">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="ead28-145">.CSV'yi güncelleştirdikten sonra değişiklikler müşterilere döndürülen ürün önerilerinde hemen yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="ead28-145">After you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="ead28-146">Uzantı, sahte öneri sonuçlarını güçlendirmek için kullanılan veri kümesini denetlemenize olanak tanıyan, 'RecoMockDataset.csv' adlı veri dosyasını içerir.</span><span class="sxs-lookup"><span data-stu-id="ead28-146">The extension contains a datafile called 'RecoMockDataset.csv', which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="ead28-147">Dosya adı, **ext.Recommendations.DemoFilePath** ayarı kullanılarak uzantı yapılandırmasıyla denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="ead28-147">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="ead28-148">Böylece, yapılandırma yoluyla değiştirilebilen mevcut birden fazla veri kümesine sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ead28-148">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="ead28-149">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ead28-149">Additional resources</span></span>

[<span data-ttu-id="ead28-150">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="ead28-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ead28-151">Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ead28-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ead28-152">Ürün önerilerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="ead28-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ead28-153">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ead28-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ead28-154">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="ead28-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ead28-155">POS'ta ürün önerileri ekleme</span><span class="sxs-lookup"><span data-stu-id="ead28-155">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ead28-156">Hareket ekranına öneriler ekleme</span><span class="sxs-lookup"><span data-stu-id="ead28-156">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ead28-157">AI-ML öneri sonuçlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ead28-157">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ead28-158">Seçkin önerileri el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="ead28-158">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ead28-159">Ürün önerileri SSS</span><span class="sxs-lookup"><span data-stu-id="ead28-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
