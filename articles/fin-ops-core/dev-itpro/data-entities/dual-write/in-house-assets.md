---
title: Servis sağlanacak şirket içi varlıklar
description: Bu konuda, Microsoft Dynamics 365 Field Service'ı hem müşteri varlıklarına, hem de şirket içi varlıklara servis sağlamak amacıyla nasıl kullanabileceğiniz açıklanmaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
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
ms.openlocfilehash: d4d681b2362c90b69007ea44c01c886f96cc1db1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568090"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="71721-103">Servis gerçekleştirilecek şirket içi varlıklar</span><span class="sxs-lookup"><span data-stu-id="71721-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="71721-104">Microsoft Dynamics 365 Field Service, müşteri varlıklarına servis sağlamak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="71721-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="71721-105">Dynamics 365 Supply Chain Management için varlık yönetimi, şirket içi kıymetlere bakım yapmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="71721-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="71721-106">Bu iki uygulamanın tümleştirilmesi, Field Service'ı hem de şirket içi varlıklara hem de müşteri varlıklarına servis sağlamak üzere kullanmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="71721-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="71721-107">Ayrıca, işelm yapılacak yerleşim veya hiyerarşiye dayalı olarak varlıkları sınıflandırabilir ve servis işlemini ayrıntılı düzeyde izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="71721-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="71721-108">Daha fazla bilgi için bkz. [Dynamics 365 Field Service ile Supply Chain Management'ı Tümleştirme](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="71721-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="71721-109">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="71721-109">Templates</span></span>

<span data-ttu-id="71721-110">Şirket içi kıymetler, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel tablo eşlemeleri koleksiyonunu içerir.</span><span class="sxs-lookup"><span data-stu-id="71721-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="71721-111">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="71721-111">Finance and Operations apps</span></span> | <span data-ttu-id="71721-112">Dynamics 365'teki model yönetimli uygulamalar</span><span class="sxs-lookup"><span data-stu-id="71721-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="71721-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="71721-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="71721-114">Varlık yönetimi varlık yaşam döngüsü modelleri</span><span class="sxs-lookup"><span data-stu-id="71721-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="71721-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="71721-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="71721-116">Varlık yönetimi varlık yaşam döngüsü durumları</span><span class="sxs-lookup"><span data-stu-id="71721-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="71721-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="71721-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="71721-118">Varlık yönetimi varlıkları</span><span class="sxs-lookup"><span data-stu-id="71721-118">Asset management assets</span></span> | <span data-ttu-id="71721-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="71721-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="71721-120">Varlık yönetimi varlık türleri</span><span class="sxs-lookup"><span data-stu-id="71721-120">Asset management asset types</span></span> | <span data-ttu-id="71721-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="71721-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="71721-122">Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü modelleri</span><span class="sxs-lookup"><span data-stu-id="71721-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="71721-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="71721-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="71721-124">Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü durumları</span><span class="sxs-lookup"><span data-stu-id="71721-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="71721-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="71721-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="71721-126">Varlık yönetimi işlem yapılacak yerleşimler</span><span class="sxs-lookup"><span data-stu-id="71721-126">Asset management functional locations</span></span> | <span data-ttu-id="71721-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="71721-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="71721-128">Varlık yönetimi işlem yapılacak yerleşim türleri</span><span class="sxs-lookup"><span data-stu-id="71721-128">Asset management functional location types</span></span> | <span data-ttu-id="71721-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="71721-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="71721-130">Varlık yönetimi üreticiler</span><span class="sxs-lookup"><span data-stu-id="71721-130">Asset management manufacturers</span></span> | <span data-ttu-id="71721-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="71721-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="71721-132">Varlık yönetimi modelleri</span><span class="sxs-lookup"><span data-stu-id="71721-132">Asset management models</span></span> | <span data-ttu-id="71721-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="71721-133">msdyn\_models</span></span> | |
| <span data-ttu-id="71721-134">Varlık yönetimi garanti</span><span class="sxs-lookup"><span data-stu-id="71721-134">Asset management warranty</span></span> | <span data-ttu-id="71721-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="71721-135">msdyn\_warranties</span></span> | |

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