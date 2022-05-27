---
title: Hareketli ortalama, geri dönüş maliyet sırası
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta hareketli ortalama hesaplamaları için geri dönüş maliyet sıraları hakkında bilgi sağlar.
author: JennySong-SH
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 1056ab771c292aebc54e229d1f14f3901f9a5d9c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674491"
---
# <a name="moving-average-fallback-cost-sequence"></a>Hareketli ortalama, geri dönüş maliyet sırası

[!include [banner](../includes/banner.md)]

Stoğunuzun maliyetini hesaplamak için kullanabileceğiniz bir yöntem _hareketli ortalama_ kullanmaktır. Her stok maddesiyle en fazla üç maliyet değeri ilişkilendirilebilir:

- **Son çıkış** – Stok eksiye düşmeden önce atanan son çıkış maliyeti
- **Etkin maliyet** – Maliyetlendirme sürümünde etkinleştirilen en son maliyet
- **Madde fiyatı** - Serbest bırakılan ürün için belirtilen maliyet

Hareketli ortalama hesaplamalarında bu maliyet değerlerinin hangisinin kullanılacağını belirlemek için, sistem değerler için tercih sırasını oluşturmak üzere _geri dönüş maliyet sırasını_ kullanır. Tercih edilen maliyet değeri kullanılamıyorsa, sistem bir sonraki tercih edilen değeri kullanır.

Microsoft Dynamics 365 Supply Chain Management'ın önceki sürümlerinde, sistem sabit bir geri dönüş maliyet sırası (_Son çıkış – Etkin maliyet – Madde fiyatı_) kullanıyordu. Sürüm 10.0.11'de bu sıra varsayılan olarak kalır. Ancak, üç adet geri dönüş maliyeti sırası arasından seçim yapmanızı sağlayan bir özelliği de açabilirsiniz. Bu özellik, özellikle negatif stok değerlerini düzenli olarak kullanan kuruluşlar için kullanışlı olabilir.

Geri dönüş maliyet sırası için seçiciyi kullanılabilir hale getirmek üzere sizin (veya bir yöneticinin), _Hareketli ortalama geri dönüş maliyeti sırası_ adlı özelliği etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanmanız gerekir.

Hareketli ortalama hesaplamaları için geri dönüş maliyet sırasını seçmek üzere aşağıdaki adımları izleyin.

1. **Parametreler** sayfasını açın.
2. **Stok muhasebesi** sekmesinde, **Hareketli ortalama** bölümünde, **Geri dönüş maliyet sırası** alanını aşağıdaki değerlerden birine ayarlayın:

    - **Son çıkış - Etkin maliyet – Madde fiyatı** – Bu sıra varsayılan sıradır. _Hareketli ortalama geri dönüş maliyet sırası_ özelliği etkin olduğunda kullanılan sırayla aynı sıradır.
    - **Etkin maliyet - Son çıkış**
    - **Etkin maliyet – Madde fiyatı** - Kuruluşlar, stoklarda düzenli olarak negatif olan ve aynı anda hareket hacmi yüksek olan iş süreçlerini kullandıklarında, performans sorunlarıyla karşılaşabilir. Bu ayar, bu performans sorunlarının etkilerini hafifletmeye yardımcı olabilir.

![Stok muhasebesi parametreleri.](media/inventory-accounting-parameters.png "Stok muhasebesi parametreleri")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]