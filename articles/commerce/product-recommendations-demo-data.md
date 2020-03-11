---
title: Tanıtım verilerini kullanarak ürün önerileri edinme
description: Bu belgeyle önceden doldurulan, ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: 1456feb0665b6ec79a36a3704f17da80ffd759a0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042792"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="ce845-103">Tanıtım verilerini kullanarak ürün önerileri edinme</span><span class="sxs-lookup"><span data-stu-id="ce845-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="ce845-104">Bu belgeyle önceden doldurulan, ve özelleştirilebilir tanıtım verileri kullanılarak Katman 1 tek taraflı ortamlarda çoklu kanal ürün önerilerinin nasıl kullanılacağına ilişkin kılavuz sunmak amaçlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ce845-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="ce845-105">Çoklu kanal ürün önerilerinde, editör tarafından düzenlenen veya program tarafından oluşturulan bir dizi sipariş edilmiş ürünlerin listesini sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ce845-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="ce845-106">Bu listeler, iş ihtiyaçlarınıza bağlı olarak birçok senaryoda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ce845-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="ce845-107">Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="ce845-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="ce845-108">Katman 2 ve daha yüksek Dynamics 365 Ortamlarında ürün önerileri, müşteri verilerine göre otomatik olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="ce845-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="ce845-109">Ürün önerileri tanıtım verilerini kullanmak, ortamda zaten sağlanmış olan herhangi bir ürün önerisi çözümünü ve bu çözümün kullanımıyla ilişkili hiçbir maliyeti devre dışı bırakmaz.</span><span class="sxs-lookup"><span data-stu-id="ce845-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="ce845-110">Katman 1 ortamlarında ürün önerilerinde yalnızca .csv dosyasında depolanan statik tanıtım verileri esas alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ce845-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="ce845-111">Bir ortamdaki ürün önerileri tanıtım verilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ce845-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="ce845-112">Ürün örnerileri demo tarhini etkinleştirmek için Müşterilerin Dynamics 365 Commerce Önizleme Tanıtım Uzantısı'nı ilgili ortama dağıtması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ce845-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="ce845-113">Böylece, ürün önerileri tanıtım verileri otomatik olarak etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ce845-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="ce845-114">Varsayılan tanıtım verileri</span><span class="sxs-lookup"><span data-stu-id="ce845-114">Default demo data</span></span>
<span data-ttu-id="ce845-115">Her bir Onebox türü ortamı, virgülle ayrılan Commerce Scale Unit'da bulunan ‘reco_demo_data.csv’ dosyasında depolanan bir dizi önceden yüklenmiş ürün önerileriyle birlikte gelir.</span><span class="sxs-lookup"><span data-stu-id="ce845-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="ce845-116">Bu veriler, aşağıdaki sütunlar boyunca yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="ce845-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="ce845-117">Sütun adı</span><span class="sxs-lookup"><span data-stu-id="ce845-117">Column name</span></span>         | <span data-ttu-id="ce845-118">Zorunlu</span><span class="sxs-lookup"><span data-stu-id="ce845-118">Mandatory</span></span>          | <span data-ttu-id="ce845-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce845-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="ce845-120">Olası Değerler</span><span class="sxs-lookup"><span data-stu-id="ce845-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ce845-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="ce845-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="ce845-123">Tanıtım veri noktasının oluşturulması gereken özel ürün önerisi listesi türü.</span><span class="sxs-lookup"><span data-stu-id="ce845-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="ce845-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="ce845-124">RecoBestSelling</span></span></li><li><span data-ttu-id="ce845-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="ce845-125">RecoNew</span></span></li><li><span data-ttu-id="ce845-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="ce845-126">RecoTrending</span></span></li><li><span data-ttu-id="ce845-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="ce845-127">RecoCart</span></span></li><li><span data-ttu-id="ce845-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="ce845-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="ce845-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="ce845-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="ce845-131">Ürün önerilerinin kullanıma sunulmasının beklendiği özel işletme birimi numarası.</span><span class="sxs-lookup"><span data-stu-id="ce845-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="ce845-132">Kategori</span><span class="sxs-lookup"><span data-stu-id="ce845-132">Category</span></span>            |                    |    <span data-ttu-id="ce845-133">Özel listenin geri döndürülmesi gerektiği kategori.</span><span class="sxs-lookup"><span data-stu-id="ce845-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="ce845-134">Hiçbir kategori belirtilmezse liste, yalnızca gezinti hiyerarşisinin üst kısmı içindir.</span><span class="sxs-lookup"><span data-stu-id="ce845-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="ce845-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="ce845-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="ce845-136">Çekirdek ürünün olması gerektiği listelerde (RecoPeopleAlsoBuy and RecoCart) ek ürünler gösterilmelidir.</span><span class="sxs-lookup"><span data-stu-id="ce845-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="ce845-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="ce845-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="ce845-139">Sonuç olarak döndürülmesi gereken ve ‘;’ ile ayrılan bir veya daha fazla ürün.</span><span class="sxs-lookup"><span data-stu-id="ce845-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="ce845-140">Tanıtım verilerini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="ce845-140">Customize demo data</span></span>
<span data-ttu-id="ce845-141">HQ'da yapılandırılan tüm ürün ve kategori bilgileriyle varsayılan tanıtım verilerini düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce845-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="ce845-142">.CSV'yi güncelleştirdiğinizde sonra müşterilere döndürülen Ürün Önerilerinde değişiklikler hemen yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="ce845-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="ce845-143">Uzantı, sahte öneri sonuçlarını güçlendirmek için kullanılan veri kümesini denetlemenize olanak tanıyan, "RecoMockDataset.csv" adlı veri dosyasını içerir.</span><span class="sxs-lookup"><span data-stu-id="ce845-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="ce845-144">Dosya adı, **ext.Recommendations.DemoFilePath** ayarı kullanılarak uzantı yapılandırmasıyla denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="ce845-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="ce845-145">Böylece, yapılandırma yoluyla değiştirilebilen mevcut birden fazla veri kümesine sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce845-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="ce845-146">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ce845-146">Additional Resources</span></span>

[<span data-ttu-id="ce845-147">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="ce845-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ce845-148">Ortam planlama</span><span class="sxs-lookup"><span data-stu-id="ce845-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
