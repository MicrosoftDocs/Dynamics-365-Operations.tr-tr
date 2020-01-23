---
title: UPPER ER işlevi
description: Bu konu, UPPER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: ed862ab823cfc3539c420d3066c9397e1e6d870e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916695"
---
# <a name="UPPER">UPPER ER işlevi</a>

[!include [banner](../includes/banner.md)]

Bu `UPPER` işlev, büyük harflere dönüştürüldükten sonra bir *dize* değeri olarak belirtilen metin dizesini döndürür.

## <a name="syntax"></a>Sözdizimi

```
UPPER (text )
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

*Dize* türünün veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`UPPER ("Sample")`, **"ÖRNEK"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)
