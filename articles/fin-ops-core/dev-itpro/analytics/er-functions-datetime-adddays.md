---
title: ADDDAYS ER işlevi
description: Bu konu, ADDDAYS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 0c420daa04b8e22504d25d317c75826f1d1914b7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747071"
---
# <a name="adddays-er-function"></a>ADDDAYS ER işlevi

[!include [banner](../includes/banner.md)]

`ADDDAYS` işlev, belirtilen başlangıç tarihinden önceki veya sonraki gün sayısı olan bir *tarih saat* değeri hesaplar.

## <a name="syntax"></a>Sözdizimi

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Bağımsız değişkenler

`datetime`: *TarihSaat*

Başlangıç tarihini gösteren bir tarih/saat değeri.

`days`: *Tamsayı*

`datetime` öncesinde veya sonrasında gün sayısı.

## <a name="return-values"></a>Dönüş değerleri

*DateTime*

Sonuç tarih/saat değeri.

## <a name="usage-notes"></a>Kullanım notları

Gelecekteki bir tarihi veren pozitif bir `days` değer. Negatif değer, geçmiş bir tarih verir.

## <a name="example-1"></a>Örnek 1

`ADDDAYS (NOW(), 7)` bugünden yedi gün sonraki tarih ve saati döndürür.

## <a name="example-2"></a>Örnek 2

`ADDDAYS (NOW(), -3)` bugünden üç gün önceki tarih ve saati döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]