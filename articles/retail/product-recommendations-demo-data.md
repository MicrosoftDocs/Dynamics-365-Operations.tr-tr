---
title: Çoklu kanal ürün önerileri tanıtım verileri
description: Bu belgeyle önceden doldurulan, ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2226553"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="a678e-103">Çoklu kanal ürün önerileri tanıtım verileri</span><span class="sxs-lookup"><span data-stu-id="a678e-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="a678e-104">Bu belgeyle önceden doldurulan, ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a678e-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="a678e-105">Çoklu kanal ürün önerilerinde, editör tarafından düzenlenen veya program tarafından oluşturulan bir dizi sipariş edilmiş ürünlerin listesini sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a678e-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="a678e-106">Bu listeler, iş ihtiyaçlarınıza bağlı olarak birçok senaryoda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a678e-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="a678e-107">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendaitons-overview.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="a678e-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="a678e-108">Katman 2 ve daha yüksek Dynamics Ortamlarında ürün önerileri, müşteri verilerine göre otomatik olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a678e-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="a678e-109">Ürün önerileri tanıtım verilerini kullanmak, ortamda zaten sağlanmış olan herhangi bir ürün önerisi çözümünü ve bu çözümün kullanımıyla ilişkili hiçbir maliyeti devre dışı bırakmaz.</span><span class="sxs-lookup"><span data-stu-id="a678e-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="a678e-110">Katman 1 ortamlarında ürün önerilerinde yalnızca .csv dosyasında depolanan statik tanıtım verileri esas alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a678e-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="a678e-111">Bir ortamdaki ürün önerileri tanıtım verilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a678e-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="a678e-112">Müşterilerin **Dynamics 365 Commerce Önizleme Tanıtım Uzantısı**'nı ilgili ortama dağıtması gerekir. Böylece, ürün önerileri tanıtım verileri otomatik olarak etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a678e-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="a678e-113">Varsayılan tanıtım verileri</span><span class="sxs-lookup"><span data-stu-id="a678e-113">Default demo data</span></span>
<span data-ttu-id="a678e-114">Her bir Onebox türü ortamı, virgülle ayrılan **‘reco_demo_data.csv’** dosyasında depolanan bir dizi önceden yüklenmiş ürün önerileriyle birlikte gelir ve Retail Server'da bu belgeyle aynı klasörde bulunur.</span><span class="sxs-lookup"><span data-stu-id="a678e-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="a678e-115">Bu veriler, aşağıdaki sütunlar boyunca yapılandırılmıştır</span><span class="sxs-lookup"><span data-stu-id="a678e-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="a678e-116">Sütun adı</span><span class="sxs-lookup"><span data-stu-id="a678e-116">Column name</span></span>         | <span data-ttu-id="a678e-117">Zorunlu</span><span class="sxs-lookup"><span data-stu-id="a678e-117">Mandatory</span></span>          | <span data-ttu-id="a678e-118">Tanım</span><span class="sxs-lookup"><span data-stu-id="a678e-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="a678e-119">Olası Değerler</span><span class="sxs-lookup"><span data-stu-id="a678e-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a678e-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="a678e-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="a678e-122">Tanıtım veri noktasının oluşturulması gereken özel ürün önerisi listesi türü.</span><span class="sxs-lookup"><span data-stu-id="a678e-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="a678e-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="a678e-123">RecoBestSelling</span></span></li><li><span data-ttu-id="a678e-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="a678e-124">RecoNew</span></span></li><li><span data-ttu-id="a678e-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="a678e-125">RecoTrending</span></span></li><li><span data-ttu-id="a678e-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="a678e-126">RecoCart</span></span></li><li><span data-ttu-id="a678e-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="a678e-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="a678e-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="a678e-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="a678e-130">Ürün önerilerinin kullanıma sunulmasının beklendiği özel işletme birimi numarası.</span><span class="sxs-lookup"><span data-stu-id="a678e-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="a678e-131">Kategori</span><span class="sxs-lookup"><span data-stu-id="a678e-131">Category</span></span>            |                    |    <span data-ttu-id="a678e-132">Özel listenin geri döndürülmesi gerektiği kategori.</span><span class="sxs-lookup"><span data-stu-id="a678e-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="a678e-133">Hiçbir kategori belirtilmezse liste, yalnızca gezinti hiyerarşisinin üst kısmı içindir.</span><span class="sxs-lookup"><span data-stu-id="a678e-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="a678e-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="a678e-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="a678e-135">Çekirdek ürünün olması gerektiği listelerde (RecoPeopleAlsoBuy and RecoCart) ek ürünler gösterilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a678e-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="a678e-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="a678e-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="a678e-138">Sonuç olarak döndürülmesi gereken ve **‘;’** ile ayrılan bir veya daha fazla ürün.</span><span class="sxs-lookup"><span data-stu-id="a678e-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="a678e-139">Tanıtım verilerini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="a678e-139">Customize demo data</span></span>
<span data-ttu-id="a678e-140">Müşteriler, HQ'da yapılandırılan tüm ürün ve kategori bilgileriyle varsayılan tanıtım verilerini düzenleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="a678e-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="a678e-141">CSV güncelleştirildikten sonra müşterilere döndürülen Ürün Önerilerinde değişiklikler hemen yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="a678e-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="a678e-142">Uzantı, müşterinin sahte öneri sonuçlarını güçlendirmek için kullanılan veri kümesini denetlemesine olanak tanıyan, "RecoMockDataset.csv" adlı veri dosyasını içerir.</span><span class="sxs-lookup"><span data-stu-id="a678e-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="a678e-143">Dosya adı, **ext.Recommendations.DemoFilePath** ayarı kullanılarak uzantı yapılandırmasıyla denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="a678e-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="a678e-144">Böylece müşteriler, yapılandırma yoluyla değiştirilebilen mevcut birden fazla veri kümesine sahip olabilirler.</span><span class="sxs-lookup"><span data-stu-id="a678e-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="a678e-145">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a678e-145">Additional resources</span></span>

[<span data-ttu-id="a678e-146">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="a678e-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="a678e-147">Ortam planlama</span><span class="sxs-lookup"><span data-stu-id="a678e-147">Environment planning</span></span>](environment-planning.md)
