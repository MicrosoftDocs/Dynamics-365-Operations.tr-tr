---
title: INT64VALUE ER işlevi
description: Bu makalede, INT64VALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 37fae9cdc5a833009b0ca1cbeb851e5e6e1b6608
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892178"
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