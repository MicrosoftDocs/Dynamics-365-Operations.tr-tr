---
title: Servis sağlanacak şirket içi varlıklar
description: Bu konuda, Microsoft Dynamics 365 Field Service'ı hem müşteri varlıklarına, hem de şirket içi varlıklara servis sağlamak amacıyla nasıl kullanabileceğiniz açıklanmaktadır.
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
ms.openlocfilehash: 040f9d26a137ebce1edc6adf28ff226b3a81e1ae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748605"
---
# <a name="in-house-assets-for-servicing"></a>Servis gerçekleştirilecek şirket içi varlıklar

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service, müşteri varlıklarına servis sağlamak üzere tasarlanmıştır. Dynamics 365 Supply Chain Management için varlık yönetimi, şirket içi kıymetlere bakım yapmak üzere tasarlanmıştır. Bu iki uygulamanın tümleştirilmesi, Field Service'ı hem de şirket içi varlıklara hem de müşteri varlıklarına servis sağlamak üzere kullanmanıza olanak tanır. Ayrıca, işelm yapılacak yerleşim veya hiyerarşiye dayalı olarak varlıkları sınıflandırabilir ve servis işlemini ayrıntılı düzeyde izleyebilirsiniz.

Daha fazla bilgi için bkz. [Dynamics 365 Field Service ile Supply Chain Management'ı Tümleştirme](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Şablonlar

Şirket içi kıymetler, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel tablo eşlemeleri koleksiyonunu içerir.

| Finance and Operations uygulamaları | Dynamics 365'teki model yönetimli uygulamalar | Tanım |
|-----------------------------|-----------------------------------|-------------|
| Varlık yönetimi varlık yaşam döngüsü modelleri | msdyn\_assetlifecyclemodels | |
| Varlık yönetimi varlık yaşam döngüsü durumları | msdyn\_assetlifecyclestates | |
| Varlık yönetimi varlıkları | msdyn\_customerassets | |
| Varlık yönetimi varlık türleri | msdyn\_customerassetcategories | |
| Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü modelleri | msdyn\_functionallocationlifecyclemodels | |
| Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü durumları | msdyn\_functionallocationlifecyclestates | |
| Varlık yönetimi işlem yapılacak yerleşimler | msdyn\_functionallocations | |
| Varlık yönetimi işlem yapılacak yerleşim türleri | msdyn\_functionallocationtypes | |
| Varlık yönetimi üreticiler | msdyn\_manufacturers | |
| Varlık yönetimi modelleri | msdyn\_models | |
| Varlık yönetimi garanti | msdyn\_warranties | |

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