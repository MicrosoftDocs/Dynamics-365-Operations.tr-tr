---
title: DAYS ER işlevi
description: Bu makalede, DAYS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 41a324ca93497f8b297c8c944f622b7829f1ceff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881244"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]