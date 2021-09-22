---
title: Birim ve birim miktarı stok günlüğünde doğru çalışmıyor
description: Birim ve birim miktarı stok günlüğünde doğru çalışmıyor
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477829"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Birim ve birim miktarı stok günlüğünde doğru çalışmıyor

## <a name="symptoms"></a>Belirtiler

Stok günlüğünde birimlerle ve miktarlarla çalışırken aşağıdaki sorunlardan biriyle veya her ikisiyle birden karşılaşabilirsiniz:

- Serbest bırakılan ürün için bir dönüştürme birimi ayarlanırken stok günlüğünde birimleri veya birim miktarlarını görmezsiniz ve stok günlüğündeki birimi değiştiremezsiniz.
- Stok günlüğünde **Miktar** ve **Birim** alanlarını görürsünüz ancak **Birim miktarı** alanını görmezsiniz. Birimi değiştirir, bir miktar girer ve günlüğü deftere naklederseniz günlük, söz konusu miktar için özgün ölçü birimini göstermeye devam eder.

## <a name="resolution"></a>Çözüm

Bu sorunu düzeltmek için şu adımları izleyin.

1. **Özellik yönetimi** çalışma alanında, *Stok günlüklerinde ölçü birimi ve birim miktarı kullanımı* özelliğinin açık olduğundan emin olun. Bu özellik, günlüğe **Birim** ve **Birim miktarı** alanlarını ekler.
1. Özellik etkinleştirildikten sonra **Miktar**, **Birim miktarı** ve **Birim** alanlarını aşağıdaki şekilde kullanın.

    - **Miktar**: Serbest bırakılan ürün için tanımlanan varsayılan birimi kullanarak miktarı belirtin. Ancak, varsayılan birimin kendisi burada gösterilmez. Varsayılan birim ile **Birim** alanında seçilen birim arasında dönüştürme işlemi ayarlandıysa, **Miktar** alanı **Birim miktarı** ve **Birim** alanlarındaki seçimlere göre otomatik olarak güncelleştirilir.
    - **Birim miktarı**: **Birim** alanında seçilen birimi kullanarak miktarı belirtin.
    - **Birim**: **Birim miktarı** alanındaki değere uygulanacak birimi seçin.
