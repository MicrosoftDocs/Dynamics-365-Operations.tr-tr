---
title: PADLEFT ER işlevi
description: Bu makalede, PADLEFT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 551b508bc6a17b1c6a08e25d5db0094713d9634f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892580"
---
# <a name="padleft-er-function"></a>PADLEFT ER işlevi

[!include [banner](../includes/banner.md)]

`PADLEFT` işlevi, belirtilen dizenin başlangıcının belirtilen karakterlerle doldurulduğu belirtilen uzunlukta bir *dize* döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Orijinal metni temsil eden bir *dize* değeri.

`length`: *Tamsayı*

Doldurulmuş dizedeki son karakter sayısını temsil eden bir *tamsayı* değeri.

`padding chars`: *Dize*

Doldurma için kullanılacak karakterler.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`PADLEFT ("1234", 10, "`&nbsp;`")`, **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"** metin dizesini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]