---
title: ROUND ER işlevi
description: Bu konu, ROUND Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce0f50cd5e544455626862e44b774dba39cf6e57
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744499"
---
# <a name="round-er-function"></a>ROUND ER işlevi

[!include [banner](../includes/banner.md)]

`ROUND` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı yuvarladıktan sonra *Gerçek* değer olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Gerçek*

Yuvarlama gereken sayısal değer.

`decimals`: *Tamsayı*

Ondalık basamak sayısını temsil eden sayısal değer.

## <a name="return-values"></a>Dönüş değerleri

*Gerçek*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Ondalık parametresinin değeri 0'dan (sıfır) büyükse, belirtilen sayı birçok `decimals` basamağa yuvarlanır.

`decimals` bağımsız değişkeni değeri **0** (sıfır) ise, belirtilen sayı en yakın çift tamsayıya yuvarlanır.

`decimals` bağımsız değişkeni değeri 0'dan (sıfır) küçükse, belirtilen sayı ondalık basamağın soluna yuvarlanır.

## <a name="example-1"></a>Örnek 1

`ROUND (1200.767, 2)` iki ondalık basamağa yuvarlar ve **1200.77** sonucunu döndürür.

## <a name="example-2"></a>Örnek 2

`ROUND (1200.767, -3)`, 1.000'in en yakın katına yuvarlar ve **1000** döndürür.

## <a name="example-3"></a>Örnek 3

`ROUND (1200.5, 0)`, en yakın çift tamsayıya yuvarlanır ve **1200** değerini döndürür, `ROUND (1201.5, 0)` de aynısını yapar ve **1202** değerini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Matematiksel işlevler](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]