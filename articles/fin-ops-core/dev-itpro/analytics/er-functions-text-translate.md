---
title: TRANSLATE ER işlevi
description: Bu makalede, TRANSLATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278456"
---
# <a name="translate-er-function"></a>TRANSLATE ER işlevi

[!include [banner](../includes/banner.md)]

`TRANSLATE` işlevi, başka bir küme için karakterlerle belirtilen metnin karakter değiştirme sonucunu içeren bir *Dize* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
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

## <a name="usage-notes"></a>Kullanım notları

`TRANSLATE` işlevi bir seferde bir karakteri değiştirir. İşlev, `text` bağımsız değişkenin ilk karakterini `pattern` bağımsız değişkenin ilk karakteriyle değiştirir, sonra ikinci karakteri değiştirir ve tamamlanana kadar aynı akışla devam eder. `text` ve `pattern` bağımsız değişkenlerden bir karakter eşleştiğinde, bu karakter `pattern` bağımsız değişkeninden gelen karakterle aynı konumda bulunan `replacement` bağımsız değişkenden gelen karakter ile değiştirilir. Bir karakter `pattern` bağımsız değişkende birden çok kez görünürse, bu karakterin ilk oluşumuna karşılık gelen `replacement` bağımsız değişkeni eşlemesi kullanılır.

## <a name="example-1"></a>Örnek 1

`TRANSLATE ("abcdef", "cd", "GH")` aşağıdaki nedenle, belirtilen **“abcdef”** metninin **"c"** karakterini `replacement` metninin **"G"**  karakteriyle değiştirir:
-   **"c"** karakteri ilk konumdaki `pattern` metinde gösterilir.
-   `replacement` metninin ilk konumu **"G"** karakterini içerir.

## <a name="example-2"></a>Örnek 2

`TRANSLATE ("abcdef", "ccd", "GH")` **"abGdef"** döndürür.

## <a name="example-3"></a>Örnek 3

`TRANSLATE ("abccba", "abc", "123")`, **"123321"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
