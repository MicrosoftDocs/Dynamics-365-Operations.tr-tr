---
title: Ürün yapılandırma modeli hesaplamalarında yanlış yuvarlanan tamsayılar
description: Ürün yapılandırma modelleri hesaplanırken tamsayı sonuçları her zaman doğru yuvarlanmaz. Bu sorunu bir ondalık özniteliği ve hesaplaması ekleyerek düzeltin.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477867"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Ürün yapılandırma modelleri hesaplanırken tamsayılar yanlış yuvarlanıyor

## <a name="symptoms"></a>Belirtiler

Bu sorun, aşağıdaki eylem dizilerini gerçekleştirdiğinizde oluşabilir:

1. Bu öznitelikleri bir üretim yapılandırma modelinde ayarlayın:

    - Giriş (tamsayı)
    - Yüzde (ondalık)
    - Sonuç (tamsayı)

2. Aşağıdaki ifadeye sahip bir hesaplama oluşturma:

    *Sonuç* = *Giriş* × *Yüzde* ÷ 100

Bu durumda, tamsayı sonucu her zaman doğru olarak yuvarlanmaz. Örneğin, girdi 1.000 ve yüzde 2,40 ise 1.000'in yüzde 2,40'ı 24 (veya ondalık biçimde 24,00) olduğundan tamsayı sonucunun 24 olmasını beklersiniz. Bunun yerine, sonuç 23 olarak gösterilir. Ancak, yüzde değeri 2,39 olduğunda, hesaplama 23 yerine 24'e yuvarlanır. Yüzde değeri 2,50 olduğunda, hesaplama beklendiği şekilde 25'e yuvarlanır.

## <a name="cause"></a>Nedeni

Bu sorun, Microsoft Solver Foundation dahili olarak sayıları kesirleri kullanarak temsil ettiğinden oluşur. Önceki örnekte, yüzdenin 2,40 olduğu hesaplamanın sonucu 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375 olarak gösterilir. .NET bu değeri tamsayı olarak verdiğinde 23 değerini döndürür.

## <a name="resolution"></a>Çözüm

Başka senaryolar buna bağlı olduğundan bu davranış değiştirilmez. Önceki örnekte, ek bir ondalık özniteliği ve hesaplamalar ekleyerek sorunu giderebilirsiniz.

Örneğin, bir üretim yapılandırması modelinde aşağıdaki öznitelikleri ayarlayın:

- Giriş (tamsayı)
- Yüzde (ondalık)
- ResultDecimal (ondalık)
- ResultInteger (tamsayı)

Bunun ardından aşağıdaki hesaplamaları ekleyebilirsiniz:

- *ResultDecimal* = *Giriş* × *Yüzde* ÷ 100
- *ResultInteger* = *ResultDecimal*
