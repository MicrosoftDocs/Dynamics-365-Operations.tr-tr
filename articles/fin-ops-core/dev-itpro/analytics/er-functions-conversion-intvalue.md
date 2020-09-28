---
title: INTVALUE ER işlevi
description: Bu konu, INTVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: c5c3e4c8bd918fa1154d2c111970d2f6d0e90e08
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743651"
---
# <a name="intvalue-er-function"></a>INTVALUE ER işlevi

[!include [banner](../includes/banner.md)]

Bu `INTVALUE` işlevi, belirtilen dizeyi temsil eden bir *Int* değeri döndürür.

## <a name="syntax-1"></a>Sözdizimi 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Sözdizimi 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Bir *Int* numarasına dönüştürülmesi gereken metin değeri.

`number`: *Gerçek* veya *tamsayı*

Bir *Int* numarasına dönüştürülmesi gereken sayısal *Gerçek* veya *Tamsayı* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Int*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Ondalık basamaklar kesilir.

## <a name="example-1"></a>Örnek 1

`INTVALUE ("100.77")`, *Int* **100** değerini döndürür.

## <a name="example-2"></a>Örnek 2

`INTVALUE (-100.77)`, *Int* **-100** değerini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tür dönüştürme işlemleri](er-functions-category-type-conversion.md)
