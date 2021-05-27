---
title: Ürün reçetesi satırlarındaki otomatik tüketim ilke ayarları dikkate alınmıyor
description: Ürün reçetesi (BOM) satırlarındaki otomatik tüketim ilke ayarları dikkate alınmıyor.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026985"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Ürün reçetesi satırlarındaki otomatik tüketim ilke ayarları dikkate alınmıyor

KB numarası: 4612725

## <a name="symptoms"></a>Belirtiler

Bu sorun, **Üretim kontrol parametreleri** sayfasının **Otomatik güncelleştirme** sekmesindeki **Otomatik ürün reçetesi tüketimi**, *Otomatik tüketim ilkesi* olarak ayarlandığında gerçekleşir. Bu ayar, bir satınalma siparişi alındığında, tüm ürün reçetesi (BOM) satırlarının otomatik olarak tüketilmesi gerektiğini belirtir. Ürün reçetesi satırlarındaki **Otomatik tüketim ilkesi** alanı *Manuel* olarak ayarlanmışsa, ürün reçetesi satırlarının otomatik olarak tüketilemeyebilir. Ancak bu sorun oluştuğunda, **Otomatik tüketim ilkesi** alanının *Manuel* olarak ayarlandığı ürün reçetesi satırları yine de otomatik olarak tüketilir.

## <a name="resolution"></a>Çözünürlük

Bu sorunla karşılaşıyorsanız, üretim kontrol parametreleriniz, ürün reçetesi satırlarındaki **Otomatik tüketim ilkesi** ayarını geçersiz kılmak üzere ayarlanmış olabilir. **Üretim denetimi parametreleri** sayfasında, **Otomatik güncelleştirme** sekmesinde, **Otomatik ürün reçetesi tüketimi** alanının değerini denetleyin. *Her zaman* olarak ayarlanmışsa, sistem tüm ürün reçetesi satırlarındaki **Otomatik tüketim ilkesi** ayarını dikkate almaz ve satırları her zaman tüketir. Sistemin, ürün reçetesi satırlarındaki **Otomatik tüketim ilkesi** ayarını uygulaması için, **Otomatik ürün reçetesi tüketimi** alanının değerini *Otomatik tüketim ilkesi* olarak değiştirin.
