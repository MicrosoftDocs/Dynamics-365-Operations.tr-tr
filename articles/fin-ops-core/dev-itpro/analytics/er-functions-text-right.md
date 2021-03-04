---
title: RIGHT ER işlevi
description: Bu konu, RIGHT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682955"
---
# <a name="right-er-function"></a>RIGHT ER işlevi

[!include [banner](../includes/banner.md)]

Bu `RIGHT` işlevi belirtilen dizenin sonundan itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Orijinal metni temsil eden bir *dize* değeri.

`number`: *Tamsayı*

Orijinal metnin sonundan itibaren döndürülmesi gereken karakter sayısı.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`RIGHT ("Sample", 3)`, **"ple"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]