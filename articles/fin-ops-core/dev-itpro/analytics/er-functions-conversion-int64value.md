---
title: INT64VALUE ER işlevi
description: Bu konu, INT64VALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042700"
---
# <a name="INT64VALUE">INT64VALUE ER işlevi</a>

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
