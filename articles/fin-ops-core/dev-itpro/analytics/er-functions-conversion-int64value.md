---
title: INT64VALUE ER işlevi
description: Bu konu, INT64VALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755408"
---
# <a name="int64value-er-function"></a>INT64VALUE ER işlevi

[!include [banner](../includes/banner.md)]

Bu `INT64VALUE` işlevi, belirtilen dizeyi temsil eden bir *Int64* değeri döndürür.

## <a name="syntax-1"></a>Sözdizimi 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Sözdizimi 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Bir *Int64* numarasına dönüştürülmesi gereken metin değeri.

`number`: *Gerçek* veya *tamsayı*

Bir *Int64* numarasına dönüştürülmesi gereken sayısal *Gerçek* veya *Tamsayı* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Int64*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Ondalık basamaklar kesilir.

## <a name="example-1"></a>Örnek 1

`INT64VALUE ("22565422744")`, *Int64* **22565422744** değerini döndürür.

## <a name="example-2"></a>Örnek 2

`INT64VALUE ( VALUE("22565422744.77"))`, *Int64* **22565422744** değerini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tür dönüştürme işlemleri](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]