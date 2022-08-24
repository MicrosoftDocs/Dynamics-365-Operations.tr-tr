---
title: Servis gerçekleştirilecek şirket içi varlıklar
description: Bu makalede, Microsoft Dynamics 365 Field Service'i hem müşteri varlıklarına hem de şirket içi varlıklara hizmet sağlamak için nasıl kullanabileceğiniz açıklanmıştır.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b3e741c85fcad2abc18879280ef7332ae091c984
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289265"
---
# <a name="in-house-assets-for-servicing"></a>Servis gerçekleştirilecek şirket içi varlıklar

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service, müşteri varlıklarına servis sağlamak üzere tasarlanmıştır. Dynamics 365 Supply Chain Management için varlık yönetimi, şirket içi kıymetlere bakım yapmak üzere tasarlanmıştır. Bu iki uygulamanın tümleştirilmesi, Field Service'ı hem de şirket içi varlıklara hem de müşteri varlıklarına servis sağlamak üzere kullanmanıza olanak tanır. Ayrıca, işelm yapılacak yerleşim veya hiyerarşiye dayalı olarak varlıkları sınıflandırabilir ve servis işlemini ayrıntılı düzeyde izleyebilirsiniz.

Daha fazla bilgi için bkz. [Dynamics 365 Field Service ile Supply Chain Management'ı Tümleştirme](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Şablonlar

Şirket içi kıymetler, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel tablo eşlemeleri koleksiyonunu içerir.

| Finance and Operations uygulamaları | Müşteri etkileşimi uygulamaları | Tanım |
|-----------------------------|-----------------------------------|-------------|
[Varlık yönetimi varlık yaşam döngüsü modelleri](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Varlık yönetimi varlık yaşam döngüsü durumları](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Varlık yönetimi varlık türleri](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Varlık yönetimi varlıkları](mapping-reference.md#125) | msdyn_customerassets | |
[Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü modelleri](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Varlık yönetimi işlem yapılacak yerleşim yaşam döngüsü durumları](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Varlık yönetimi işlem yapılacak yerleşim türleri](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Varlık yönetimi işlem yapılacak yerleşimler](mapping-reference.md#136) | msdyn_functionallocations | |
[Varlık yönetimi üreticiler](mapping-reference.md#153) | msdyn_manufacturers | |
[Varlık yönetimi modelleri](mapping-reference.md#154) | msdyn_models | |
[Varlık yönetimi garanti](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
