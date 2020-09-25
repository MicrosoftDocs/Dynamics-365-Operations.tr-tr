---
title: MID ER işlevi
description: Bu konu, MID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744731"
---
# <a name="mid-er-function"></a>MID ER işlevi

[!include [banner](../includes/banner.md)]

Bu `MID` işlev belirtilen pozisyondan başlayarak belirtilen dizenin başından itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Karakterlerin alınacağı metni belirten bir *dize* değeri.

`starting position`: *Tamsayı*

Belirtilen metinden ilk karakterin döndürülmesi gereken konumu belirten bir *tamsayı* değeri.

`number of characters`: *Tamsayı*

Belirtilen pozisyondan başlayarak döndürülmesi gereken karakter sayısını belirten bir *tamsayı* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

`starting position` bağımsız değişkenin değeri 0 (sıfır) değerinden küçükse, döndürülen karakterler belirtilen dizedeki ilk konumdan sayılır.

`starting position` bağımsız değişkenin değeri belirtilen dizenin uzunluğunu aşarsa, boş bir dize döndürülür.

## <a name="example"></a>Örnek

`MID ("Sample", 2, 3)`, **"amp"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)
