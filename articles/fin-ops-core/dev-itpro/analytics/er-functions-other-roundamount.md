---
title: ROUNDAMOUNT ER işlevi
description: Bu konu, ROUNDAMOUNT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 5903f562b5f266572f999756539fa7b9ef145023
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041343"
---
# <a name="ROUNDAMOUNT">ROUNDAMOUNT ER işlevi</a>

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

`decimals` parametre sıfır olduğunda, bu işlev varsayılan yuvarlama değerine yuvarlanır. `round rule` parametre, **RoundOffType.Ordinary**olarak ayarlandığında, varsayılan yuvarlama değeri **0,01**'dir. Aksi durumda, varsayılan yuvarlama değeri **1,0**'dir.

`round rule` parametre, **RoundOffType.Ordinary** olarak ayarlandığında bu işlev normal olarak en yakın yuvarlama miktarına yuvarlanır.

`round rule` parametre, **RoundOffType.RoundDown** olarak ayarlandığında bu işlev sıfıra en yakın yuvarlama miktarına yuvarlanır.

`round rule` parametre, **RoundOffType.RoundUp** olarak ayarlandığında bu işlev sıfırdan en uzak en yakın yuvarlama miktarına yuvarlanır.

`round rule` parametresi **RoundOffType.Ordinary** olarak ayarlandığında, bu işlev [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel işlevi ve [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ işlevi gibi davranır.

## <a name="remarks"></a>Açıklamalar

Sayısal değeri belirtilen sayıda ondalık basamağa yuvarlamak için [ROUND](er-functions-mathematical-round.md) işlevini kullanın.

## <a name="example"></a>Örnek

**model.RoundOff** parametresi **RoundOffType.Ordinary** olarak ayarlandı, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 döndürür. 

**model.RoundOff** parametresi **RoundOffType.RoundDown** olarak ayarlandı, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 döndürür. 

**model.RoundOff** parametresi **RoundOffType.RoundUp** olarak ayarlandı, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4 döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)

[Matematik işlevi](er-functions-category-mathematical.md)
