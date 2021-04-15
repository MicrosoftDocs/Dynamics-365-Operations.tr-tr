---
title: Müşteri bağlılık programı kartları ve ödül puanları
description: Bu konuda, müşteri bağlılık programı kartları ve çift yazmadaki ödül puanlarıyla ilgili verilerin tümleştirilmesi açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
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
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747999"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Müşteri bağlılık programı kartları ve ödül puanları

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

İşletmeler, müşteri alışverişi ve harcama alışkanlıkları temel alınarak müşterileri sınıflandırmakta ve karmaşık servisler sağlıyor. Örneğin Dynamics 365 Commerce, müşteri bağlılık programı kartlarını, ödüllendirme puanlarını, bağlılık programı tabanlı fiyatlandırmayı ve ödül tabanlı alışveriş deneyimlerini kolaylaştırmak ve işlemek için gerekli altyapıya ve işlevlere sahiptir. Commerce'teki müşteri bağlılık programı kartları ve ödül puanları Dataverse'e eşitlendiğinde, müşteri etkileşimi uygulamaları bu verileri kullanabilir. Örneğin, Dynamics 365 Customer Service kullanıcıları, verileri yardım masasıyla aynı Gelişmiş hizmetleri sağlamak için kullanabilir.

## <a name="templates"></a>Şablonlar

| Finance and Operations uygulamaları | Dynamics 365'teki model yönetimli uygulamalar | Tanım |
|-----------------------------|-----------------------------------|-------------|
| Bağlılık programı kartı                | msdyn\_loyaltycards               | Bu şablon müşteri bağlılık programı kartılarıyla ilgili bilgileri eşitler. |
| Bağlılık programı ödül puanları       | msdyn\_loyaltyrewardpoints        | Bu şablon müşteri ödül puanlarıyla ilgili bilgileri eşitler. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]