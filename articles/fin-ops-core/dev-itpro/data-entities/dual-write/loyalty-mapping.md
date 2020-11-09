---
title: Müşteri bağlılık programı kartları ve ödül puanları
description: Bu konu, müşteri bağlılık programı kartları ve Finance and Operations uygulamaları ile Common Data Service arasındaki ödül puanlarıyla ilgili verilerin tümleştirilmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998026"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Müşteri bağlılık programı kartları ve ödül puanları

[!include [banner](../../includes/banner.md)]



İşletmeler, müşteri alışverişi ve harcama alışkanlıkları temel alınarak müşterileri sınıflandırmakta ve karmaşık servisler sağlıyor. Microsoft Dynamics 365 uygulama paketinde, Dynamics 365 Commerce müşteri bağlılık programı kartlarını, ödüllendirmeyi, bağlılık programı tabanlı fiyatlandırmayı ve ödül tabanlı alışveriş deneyimlerini kolaylaştırmak ve işlemek için gerekli altyapıyı ve işlevleri vardır. Commerce'teki müşteri bağlılık programı kartları ve ödül puanları Common Data Service'e eşitlendiğinde Dynamics 365'teki modele dayalı uygulamalar bu verileri kullanabilir. Örneğin, Dynamics 365 Customer Service kullanıcıları, verileri yardım masasıyla aynı Gelişmiş hizmetleri sağlamak için kullanabilir.

## <a name="templates"></a>Şablonlar

| Finance and Operations uygulamaları | Dynamics 365'teki model yönetimli uygulamalar | Tanım |
|-----------------------------|-----------------------------------|-------------|
| Bağlılık programı kartı                | msdyn\_loyaltycards               | Bu şablon müşteri bağlılık programı kartılarıyla ilgili bilgileri eşitler. |
| Bağlılık programı ödül puanları       | msdyn\_loyaltyrewardpoints        | Bu şablon müşteri ödül puanlarıyla ilgili bilgileri eşitler. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
