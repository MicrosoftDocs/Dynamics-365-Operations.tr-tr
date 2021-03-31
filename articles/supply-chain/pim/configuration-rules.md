---
title: Konfigürasyon kuralları
description: Bu makalede, yapılandırma kuralları hakkında genel bilgiler sağlanmıştır. Yapılandırma kuralları, boyut tabanlı yapılandırma teknolojisini kullanan ürünler için ürün reçetesindeki (BOM) maddeler arasındaki ilişkileri tanımlar.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac3515837df45b65121ebec72a32ac98d740796a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221883"
---
# <a name="configuration-rules"></a>Konfigürasyon kuralları

[!include [banner](../includes/banner.md)]

Bu makalede, yapılandırma kuralları hakkında genel bilgiler sağlanmıştır. Yapılandırma kuralları, boyut tabanlı yapılandırma teknolojisini kullanan ürünler için ürün reçetesindeki (BOM) maddeler arasındaki ilişkileri tanımlar.

Boyut bazlı yapılandırma modelleri tanımladığınızda yapılandırma kuralları kullanılabilir. Yapılandırma kuralları ürün reçetesindeki belirli madde kombinasyonlarını zorunlu kılmak veya yasaklamak için kullanılır. Bir ürün reçetesi oluşturulduktan ve ilgili maddeler kendi ilgili yapılandırma gruplarına atandıktan sonra, bir veya daha fazla yapılandırma kuralı tanımlanabilir. İki madde birbirine aitse, dahil etmeyi sağlamak **Seç** işleci kullanılır. İki madde karşılıklı olarak birbirini dışlıyorsa, **Seçimi Kaldır** işleci dışlama sağlamak için kullanılır.  

**Not:** Bu bilgiler, yalnızca boyut bazlı yapılandırma teknolojisi kullanan ana ürünler için geçerlidir.  

Yapılandırma kurallarında sonradan yapılan değişiklikler mevcut yapılandırmaları etkilemez. Ancak, yeni bir yapılandırma tanımlamadan önce kuralları belirlemek veya kuralların değiştirildiğini düşündüğünüzde bunları kontrol etmek önemlidir.  

**Not:** **Seç** yöntemi için, türetilen yapılandırma grubu, madde numarası ve yapılandırma otomatik olarak seçilir. **Seçimi Kaldır** yöntemi için, türetilen yapılandırma grubu, madde numarası ve yapılandırma seçilemez.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Boyut tabanlı ürün yapılandırmasına genel bakış](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]