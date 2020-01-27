---
title: ADDDAYS ER işlevi
description: Bu konu, ADDDAYS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916465"
---
# <a name="ADDDAYS">ADDDAYS ER işlevi</a>

[!include [banner](../includes/banner.md)]

`ADDDAYS` işlev, belirtilen başlangıç tarihinden önceki veya sonraki gün sayısı olan bir *tarih saat* değeri hesaplar.

## <a name="syntax"></a>Sözdizimi

```
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
