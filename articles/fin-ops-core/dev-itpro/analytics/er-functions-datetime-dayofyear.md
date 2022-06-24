---
title: DAYOFYEAR ER işlevi
description: Bu makalede, DAYOFYEAR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: fc4d1d3293c31b1b89a7390c8ac313e1407d433e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848794"
---
# <a name="dayofyear-er-function"></a>DAYOFYEAR ER işlevi

[!include [banner](../includes/banner.md)]

`DAYOFYEAR` işlev, Ocak 1 ve belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Bağımsız değişkenler

`date`: *Tarih*

Gün sayısı hesaplaması için kullanılacak tarihi temsil eden bir tarih değeri.

## <a name="return-values"></a>Dönüş değerleri

*Tamsayı*

Sonuç sayısal değeri.

## <a name="example-1"></a>Örnek 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))`, **61** döndürür.

## <a name="example-2"></a>Örnek 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))`, **1** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]