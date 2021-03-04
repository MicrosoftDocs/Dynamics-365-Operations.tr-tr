---
title: TRIM ER işlevi
description: Bu konu, TRIM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 908da840ffcb94f4a60bb41ce041f5f263c921eb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688386"
---
# <a name="trim-er-function"></a>TRIM ER işlevi

[!include [banner](../includes/banner.md)]

`TRIM` işlevi, belirtilen metin dizesini baştaki ve sondaki boşluklar kesildikten ve sözcükler arasındaki birden fazla boşluk kaldırıldıktan sonra *Dize* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
TRIM (text )
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

*Dize* türünün veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")`, **"Örnek metin"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]