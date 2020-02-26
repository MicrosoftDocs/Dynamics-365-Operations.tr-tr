---
title: Ürün önerilerine genel bakış
description: Bu konuda ürün önerileri hakkında genel bilgiler verilmiştir. Ürün önerileri, müşterilerin istedikleri ürünleri ve hatta satın almayı amaçlamadıkları ürünleri kolayca ve hızlı bir şekilde bulmasına olanak tanır.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024991"
---
# <a name="product-recommendations-overview"></a>Ürün önerilerine genel bakış

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce, e-ticaret Web sitesi ve satış noktası (POS) aygıtında ürün önerilerini göstermek için kullanılabilir. Ürün önerileri, bir müşterinin ilgilendiği öğelerdir. Öneriler, çevrimiçi ve fiziksel mağazalardaki diğer müşterilerin satın alma eğilimlerine dayanır.

Ürün önerileri, müşterilerin kendilerine hizmet veren bir deneyim sağlarken istedikleri ürünleri kolayca ve hızlı bir şekilde bulmasına olanak tanır. Çapraz satış ve kaplamalı ürünler, müşterilerin başlangıçta satın almayı amaçlamadıklarından daha fazla ürün bulmasına yardımcı olmak için de kullanılabilir. Öneriler, ürün bulma ile ilgili yardım için kullanıldığında, daha fazla dönüştürme fırsatı oluşturabilir, satış gelirini artırabilir ve hatta müşteri memnuniyetini ve korunmasını artırmaya yardımcı olabilirler.

Ticari olarak, Ürün önerilerinde büyük ölçekli Microsoft önerileri makine öğrenme teknolojileriyle desteklenmektedir.


## <a name="scenarios"></a>Senaryolar

Ürün önerileri aşağıdaki senaryoları için etkinleştirilir.

- **E-ticaret 'da gözatma veya iniş sayfası için herhangi bir depolama sayfasında:** Müşteriler veya mağaza işbirlikçileri bir mağaza sayfasını ziyaret ederken, öneri altyapısı **yeni**, **en iyi satış** ve **trend** listelerinde ürünler önerebilir.
- **Ürün Ayrıntıları sayfasında:** müşteriler veya mağaza işbirlikçileri bir **ürün ayrıntıları** sayfasını ziyaret ederken, öneri altyapısı da büyük olasılıkla satın alınacak ek maddeleri önerir. Bu öğeler, **kişiler bunları da sevdi** listesinde görünür.
- **Hareket sayfasında veya kullanıma al sayfasında:** öneri altyapısı maddeleri sepetteki tüm madde listesine göre önerir. Bu maddeler **sık kullanılan bir arada** bulunan listesinde görünür.
- **Kişiselleştirilmiş öneriler:** Tacirler, varolan liste senaryolarının o müşteriye dayalı olarak kişiselleştirilmelerini sağlayan yeni işlevlere ek olarak, oturum açmış, **sizin için kişiselleştirilmiş** bir çekme müşterilerine olanak sağlayabilir. Daha fazla bilgi edinmek için, lütfen belgelerine bakın: [kişiselleştirilmiş yeniden yükleme özelliğini etkinleştirin.](personalized-recommendations.md)

## <a name="recommendation-service"></a>Öneri servisi

Ürün önerileri aşağıdaki şekilde öneriler makine öğrenme teknolojilerini kullanır:

- Öneri servisinin tarafından istenen biçimdeki veriler Commerce işlem veritabanından çıkarılması ve Varlık deposuna göndermesi gerekir.
- Öneri Servisi, verileri **Bunları da sevdi**, **sık birlikte satın alınan**, **yeni**, **en iyi satış**ve **trend** listeleri gibi kişiler için öneri modelleri eğitmek üzere kullanır.

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerini etkinleştirme](enable-product-recommendations.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

[Ürün topluluğu modülüne genel bakış](product-collection-module-overview.md)

[Seçkin ürün önerisi listeleri oluşturma](create-editorial-recommendation-lists.md)

[AI-ML tabanlı ürün önerisi sonuçlarını yönetme](modify-product-recommendation-results.md)

[Sayfalarına ürün önerileri listesi ekleme](add-reco-list-to-page.md)
