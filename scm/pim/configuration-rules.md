---
title: "Konfigürasyon kuralları"
description: "Bu makalede, yapılandırma kuralları hakkında genel bilgiler sağlanmıştır. Yapılandırma kuralları, boyut tabanlı yapılandırma teknolojisini kullanan ürünler için ürün reçetesindeki (BOM) maddeler arasındaki ilişkileri tanımlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 271a780eec291455b433c0767246d79cb965ce02
ms.lasthandoff: 03/31/2017


---

# <a name="configuration-rules"></a>Konfigürasyon kuralları

Bu makalede, yapılandırma kuralları hakkında genel bilgiler sağlanmıştır. Yapılandırma kuralları, boyut tabanlı yapılandırma teknolojisini kullanan ürünler için ürün reçetesindeki (BOM) maddeler arasındaki ilişkileri tanımlar.

Boyut bazlı yapılandırma modelleri tanımladığınızda yapılandırma kuralları kullanılabilir. Yapılandırma kuralları ürün reçetesindeki belirli madde kombinasyonlarını zorunlu kılmak veya yasaklamak için kullanılır. Bir ürün reçetesi oluşturulduktan ve ilgili maddeler kendi ilgili yapılandırma gruplarına atandıktan sonra, bir veya daha fazla yapılandırma kuralı tanımlanabilir. İki madde birbirine aitse, dahil etmeyi sağlamak **Seç** işleci kullanılır. İki madde karşılıklı olarak birbirini dışlıyorsa, **Seçimi Kaldır** işleci dışlama sağlamak için kullanılır.  

**Not:** Bu bilgiler, yalnızca boyut bazlı yapılandırma teknolojisi kullanan ana ürünler için geçerlidir.  

Yapılandırma kurallarında sonradan yapılan değişiklikler mevcut yapılandırmaları etkilemez. Ancak, yeni bir yapılandırma tanımlamadan önce kuralları belirlemek veya kuralların değiştirildiğini düşündüğünüzde bunları kontrol etmek önemlidir.  

**Not:** **Seç** yöntemi için, türetilen yapılandırma grubu, madde numarası ve yapılandırma otomatik olarak seçilir. **Seçimi Kaldır** yöntemi için, türetilen yapılandırma grubu, madde numarası ve yapılandırma seçilemez.

<a name="see-also"></a>Ayrıca bkz.
--------

[Boyuta dayalı ürün yapılandırma](dimension-based-product-configuration.md)


