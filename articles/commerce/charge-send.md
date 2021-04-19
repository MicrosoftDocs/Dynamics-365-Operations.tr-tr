---
title: Gönderimle görevlendir özelliğini kullanarak siparişleri başka bir mağazaya sevk etme
description: Bu konuda Gönderimle görevlendir özelliği açıklanmaktadır.
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: b9e0c4f55fd823bf7471edfe6ce1d424b0179d21
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800483"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Gönderimle görevlendir özelliğini kullanarak siparişleri başka bir mağazaya sevk etme

[!include [banner](includes/banner.md)]

Commerce'teki Gönderimle görevlendirme özelliğiyle, müşteri siparişleri bir mağazadan alınabilir ve başka bir mağazadan sevk edilebilir.

Satış noktası (POS) istemcisindeki müşteri siparişleri birden fazla karşılama seçeneğini destekler. Karşılama seçeneklerine örnek olarak aşağıdakiler verilebilir:

- Farklı bir tarihte aynı mağazadan alma.
- Aynı tarihte veya farklı bir tarihte farklı bir mağazadan alma.
- Mağazaya atanan varsayılan sevk deposundan sevk etme ve belirli bir tarihte teslim etme.

Gönderimle görevlendir özelliği şu POS işlemlerini kullanır: Tüm ürünleri sevk et ve Seçilen ürünleri sevk et. Bu, mağaza görevlisinin, siparişin veya sipariş satırının karşılanacağı "sevkiyat çıkış yeri" konumunu seçmesine olanak tanır. Varsayılan olarak, "sevkiyat çıkış yeri" konumu mağazayla ilişkili sevkiyat deposudur. Ancak, mağaza görevlisi bu konumu değiştirebilir ve mağazaya atanmış mağaza konumlandırıcı grubunda tanımlanan herhangi bir mağazayı seçebilir.

"Sevkiyat varış yeri" adresini seçme özelliği değişmez.

Sipariş satırını karşılamak için kullanılabilecek sevkiyat yöntemleri ürünler ve adresler için geçerli teslimat modlarının yapılandırmasını temel alır. Geçerli teslimat modlarıyla ilgili kurallar yalnızca Headquarters (HQ) içinde korunacağından, POS istemcisi bir sevkiyat satırı için geçerli teslim modlarını getirmek üzere gerçek zamanlı bir çağrı yapar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]