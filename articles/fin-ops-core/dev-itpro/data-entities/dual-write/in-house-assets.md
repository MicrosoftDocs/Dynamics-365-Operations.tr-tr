---
title: Servis gerçekleştirilecek şirket içi varlıklar
description: Bu konuda, Microsoft Dynamics 365 Field Service'i hem müşteri varlıklarına hem de şirket içi varlıklara hizmet sağlamak için nasıl kullanabileceğiniz açıklanmıştır.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941426"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="b1124-103">Servis gerçekleştirilecek şirket içi varlıklar</span><span class="sxs-lookup"><span data-stu-id="b1124-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b1124-104">Microsoft Dynamics 365 Field Service, müşteri varlıklarına servis sağlamak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b1124-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="b1124-105">Dynamics 365 Supply Chain Management için varlık yönetimi, şirket içi kıymetlere bakım yapmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b1124-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="b1124-106">Bu iki uygulamanın tümleştirilmesi, Field Service'ı hem de şirket içi varlıklara hem de müşteri varlıklarına servis sağlamak üzere kullanmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b1124-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="b1124-107">Ayrıca, işelm yapılacak yerleşim veya hiyerarşiye dayalı olarak varlıkları sınıflandırabilir ve servis işlemini ayrıntılı düzeyde izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1124-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="b1124-108">Daha fazla bilgi için bkz. [Dynamics 365 Field Service ile Supply Chain Management'ı Tümleştirme](/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="b1124-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="b1124-109">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="b1124-109">Templates</span></span>

<span data-ttu-id="b1124-110">Şirket içi kıymetler, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel tablo eşlemeleri koleksiyonunu içerir.</span><span class="sxs-lookup"><span data-stu-id="b1124-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="b1124-111">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="b1124-111">Finance and Operations apps</span></span> | <span data-ttu-id="b1124-112">Dynamics 365'teki model yönetimli uygulamalar</span><span class="sxs-lookup"><span data-stu-id="b1124-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="b1124-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1124-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="b1124-114">Varlık yönetimi varlık yaşam döngüsü modelleri</span><span class="sxs-lookup"><span data-stu-id="b1124-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="b1124-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="b1124-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="b1124-116">Varlık yönetimi varlık yaşam döngüsü durumları</span><span class="sxs-lookup"><span data-stu-id="b1124-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="b1124-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="b1124-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="b1124-118">Varlık yönetimi varlıkları</span><span class="sxs-lookup"><span data-stu-id="b1124-118">Asset management assets</span></span> | <span data-ttu-id="b1124-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="b1124-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="b1124-120">Varlık yönetimi varlık türleri</span><span class="sxs-lookup"><span data-stu-id="b1124-120">Asset management asset types</span></span> | <span data-ttu-id="b1124-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="b1124-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="b1124-122">Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü modelleri</span><span class="sxs-lookup"><span data-stu-id="b1124-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="b1124-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="b1124-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="b1124-124">Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü durumları</span><span class="sxs-lookup"><span data-stu-id="b1124-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="b1124-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="b1124-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="b1124-126">Varlık yönetimi işlem yapılacak yerleşimler</span><span class="sxs-lookup"><span data-stu-id="b1124-126">Asset management functional locations</span></span> | <span data-ttu-id="b1124-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="b1124-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="b1124-128">Varlık yönetimi işlem yapılacak yerleşim türleri</span><span class="sxs-lookup"><span data-stu-id="b1124-128">Asset management functional location types</span></span> | <span data-ttu-id="b1124-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="b1124-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="b1124-130">Varlık yönetimi üreticiler</span><span class="sxs-lookup"><span data-stu-id="b1124-130">Asset management manufacturers</span></span> | <span data-ttu-id="b1124-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="b1124-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="b1124-132">Varlık yönetimi modelleri</span><span class="sxs-lookup"><span data-stu-id="b1124-132">Asset management models</span></span> | <span data-ttu-id="b1124-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="b1124-133">msdyn\_models</span></span> | |
| <span data-ttu-id="b1124-134">Varlık yönetimi garanti</span><span class="sxs-lookup"><span data-stu-id="b1124-134">Asset management warranty</span></span> | <span data-ttu-id="b1124-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="b1124-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]