---
title: DAYS ER işlevi
description: Bu konu, DAYS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47d992d061f8664a55332024ee5c6cd41e4bc495
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743579"
---
# <a name="days-er-function"></a>DAYS ER işlevi

[!include [banner](../includes/banner.md)]

`DAYS` işlev, belirli bir tarihte ve ikinci belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Bağımsız değişkenler

`date 1`: *Tarih*

Gün sayısı hesaplaması için başlangıç tarihi temsil eden bir tarih değeri.

`date 2`: *Tarih*

Gün sayısı hesaplaması için bitiş tarihi temsil eden bir tarih değeri.

## <a name="return-values"></a>Dönüş değerleri

*Tamsayı*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

`DAYS` işlevi, ilk tarih ikinci tarihten sonra olduğunda pozitif bir değer döndürür; ilk tarih ikinci tarihle aynı olduğunda **0** (sıfır) değerini döndürür veya ilk tarih ikinci tarihten önceyse, negatif değer döndürür.

## <a name="example"></a>Örnek

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))`, **-1** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)
