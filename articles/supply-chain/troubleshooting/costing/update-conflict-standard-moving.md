---
title: Stok değerleme yöntemi standart maliyet veya hareketli ortalama olduğunda güncelleştirme çakışması oluşuyor
description: Stok değerleme yöntemi standart maliyet veya hareketli ortalama olduğunda güncelleştirme çakışması oluşuyor
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477878"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Stok değerleme yöntemi standart maliyet veya hareketli ortalama olduğunda güncelleştirme çakışması oluşuyor

## <a name="symptoms"></a>Belirtiler

Ölçeklenebilirlik ve performans için paralel olarak stok günlükleri, satınalma siparişi faturaları veya satış siparişi faturaları gibi belgeleri deftere naklettiğinizde, güncelleştirme çakışmasıyla ilgili hata iletisi alabilirsiniz ve belgelerden bazıları deftere nakledilmeyebilir. Bu sorun, stok değerleme yöntemi *Standart maliyet* veya *Hareketli ortalama* olduğunda gerçekleşebilir. Her iki yöntem de kalıcı maliyetlendirme yöntemidir. Başka bir deyişle, son maliyet deftere nakil sırasında belirlenir.

*Hareketli ortalama* yöntemini kullanıyorsanız, hata iletisi aşağıdaki örneğe benzer:

> Orantılı gider hesaplamasından sonra xx.xx stok değeri beklenmez

*Standart maliyet* yöntemini kullanıyorsanız, hata iletisi aşağıdaki örneğe benzer:

> Standart maliyet, güncelleştirmeden sonraki mali stok değeriyle eşleşmez. Değer = xx.xx, Miktar = yy.yy, Standart maliyet = zz.zz

## <a name="workaround"></a>Geçici çözüm

Microsoft sorunu düzeltmek üzere bir çözüm yayınlayana kadar, bu hataları önlemek veya azaltmak için aşağıdaki geçici çözümleri kullanabilirsiniz:

- Başarısız belgeleri yeniden deftere nakledin.
- Daha az satır içeren belgeler oluşturun.
- Standart maliyette ondalık değerler kullanmaktan kaçının. Standart maliyeti, **Fiyat miktarı** alanı *1* olarak ayarlanacak şekilde tanımlamaya çalışın. *1*'den yüksek bir **Fiyat miktarı** değeri belirtmeniz gerekiyorsa birim standart maliyetindeki ondalık basamak sayısını en aza indirmeye çalışın. (İdeal olarak, ikiden az ondalık basamak olmalıdır.) Örneğin, standart maliyet ayarlarını şu şekilde ayarlamaktan kaçının: **Fiyat** = *10* ve **Fiyat miktarı** = *3*, çünkü bunlar 3,333333 (ondalık değer devam eder) değerinde bir birim standart maliyeti oluşturur.
- Birçok belgede, aynı ürün ve mali stok boyutları birleşimini içeren birden çok satırı kullanmaktan kaçının.
- Paralelleşme derecesini azaltın. (Bu durumda sisteminiz daha hızlı olabilir, çünkü daha az güncelleştirme çakışması ve yeniden deneme gerçekleştirilir.)
