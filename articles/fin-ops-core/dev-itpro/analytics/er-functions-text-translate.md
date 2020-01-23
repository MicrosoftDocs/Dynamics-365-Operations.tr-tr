---
title: TRANSLATE ER işlevi
description: Bu konu, TRANSLATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916718"
---
# <a name="TRANSLATE">TRANSLATE ER işlevi</a>

[!include [banner](../includes/banner.md)]

`TRANSLATE` işlev, belirtilen metin dizesini bir bütün veya bir kısmı başka bir dizeyle değiştirildikten sonra *dize* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

*Dize* türünün veri kaynağının geçerli yolu.

`pattern`: *Dize*

Metnin değiştirilmesi gerekir.

`replacement`: *Dize*

Yerine konacak metin.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`TRANSLATE ("abcdef", "cd", "GH")`, **"cd"** deseni değiştirir, şunun ile: **"GH"** ve bunu döndürür: **"abGHef"**.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)
