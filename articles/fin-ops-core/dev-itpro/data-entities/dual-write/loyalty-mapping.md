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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172981"
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
