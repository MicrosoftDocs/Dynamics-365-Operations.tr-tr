---
title: ROUNDAMOUNT ER işlevi
description: Bu makalede, ROUNDAMOUNT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 0e4de43f865ca21822ab2c0c345026d2e9113ca2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286044"
---
# <a name="roundamount-er-function"></a>ROUNDAMOUNT ER işlevi

[!include [banner](../includes/banner.md)]

`ROUNDAMOUNT` işlev, belirtilen yuvarlama kuralına göre başka sayının en yakın katına belirtilen sayının yuvarlanmasının sonucu olarak *gerçek* bir değer döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Tam* veya *Gerçek*

Yuvarlama gereken sayısal değer.

`decimals`: *Tam* veya *Gerçek*

`number` parametre değerinin bir katına yuvarlanması gereken sayı.

`round rule`: *Numaralandırma değeri*

Yuvarlama kuralını tanımlayan **RoundOffType** sabit listesinin numaralandırma değeri. Bu numaralandırma aşağıdaki değerleri sağlar:

- Normal (normal)
- Aşağı (AŞAĞIYUVARLA)
- Yukarı yuvarlama (YukarıYuvarla)

## <a name="return-values"></a>Dönüş değerleri

*Gerçek*

Sonuçta elde edilen sayısal değer `decimals` parametrenin belirttiği değerin bir katları olur ve `number` parametre tarafından belirtilen değere en yakın değerdir.

## <a name="usage-notes"></a>Kullanım notları

`number` parametre sıfır olduğunda bu işlev her zaman sıfır döndürür.

`decimals` parametre sıfır olduğunda, bu işlev varsayılan yuvarlama değerine yuvarlanır. `round rule` parametre, **RoundOffType.Ordinary** olarak ayarlandığında, varsayılan yuvarlama değeri **0,01**'dir. Aksi durumda, varsayılan yuvarlama değeri **1,0**'dir.

`round rule` parametre, **RoundOffType.Ordinary** olarak ayarlandığında bu işlev normal olarak en yakın yuvarlama miktarına yuvarlanır.

`round rule` parametre, **RoundOffType.RoundDown** olarak ayarlandığında bu işlev sıfıra en yakın yuvarlama miktarına yuvarlanır.

`round rule` parametre, **RoundOffType.RoundUp** olarak ayarlandığında bu işlev sıfırdan en uzak en yakın yuvarlama miktarına yuvarlanır.

`round rule` parametresi **RoundOffType.Ordinary** olarak ayarlandığında, bu işlev [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel işlevi ve [ROUND](../dev-ref/xpp-math-run-time-functions.md#round) X++ işlevi gibi davranır.

## <a name="remarks"></a>Açıklamalar

Sayısal değeri belirtilen sayıda ondalık basamağa yuvarlamak için [ROUND](er-functions-mathematical-round.md) işlevini kullanın.

## <a name="example"></a>Örnek

**model.RoundOff** parametresi **RoundOffType.Ordinary** olarak ayarlandı, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 döndürür. 

**model.RoundOff** parametresi **RoundOffType.RoundDown** olarak ayarlandı, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 döndürür. 

**model.RoundOff** parametresi **RoundOffType.RoundUp** olarak ayarlandı, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4 döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)

[Matematik işlevi](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
