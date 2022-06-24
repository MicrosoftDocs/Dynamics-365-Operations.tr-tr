---
title: REPLACE ER işlevi
description: Bu makalede, REPLACE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 6c2b1ba82d61a3c163f1d657035b66ace9f15c77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878385"
---
# <a name="replace-er-function"></a>REPLACE ER işlevi

[!include [banner](../includes/banner.md)]

`REPLACE` işlev, belirtilen metin dizesini bir bütün veya bir kısmı başka bir dizeyle değiştirildikten sonra *dize* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

*Dize* türünün veri kaynağının geçerli yolu.

`pattern`: *Dize*

`regular expression flag` Bağımsız değişken, **yanlış** ise, bu bağımsız değişken değiştirilmesi gereken metni içerir.

`regular expression flag` Bağımsız değişken **doğru** ise, bu bağımsız değişken hem arama desenini hem de yerine konacak metni tanımlayan normal bir ifade içerir.

`replacement`: *Dize*

`regular expression flag` Bağımsız değişken, **yanlış** ise, bu bağımsız değişken yerine geçecek olarak kullanılan metni içerir.

`regular expression flag` Bağımsız değişken **doğru** ise, bu bağımsız değişken kullanılmaz.

`regular expression flag`: *Boole*

Değişiklik yapmak için normal bir ifadenin kullanılmış olup olmadığını gösteren *Boole* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

`regular expression flag` bağımsız değişken **doğru** ise, `pattern` bağımsız değişken tarafından belirtilen normal ifade uygulanarak bu işlev belirtilen dizeyi değiştirildikten sonra döndürür. Bu düzenli ifade, değiştirilmesi gereken karakterleri bulmakta kullanılır.

`regular expression flag` bağımsız değişkeni **FALSE** ise, bu işlev `pattern` bağımsız değişkeninde tanımlanan karakter kümesin `replacement` bağımsız değişkeninin karakterleriyle değiştirildikten sonra belirtilen dizeyi döndürür. 

## <a name="example-1"></a>Örnek 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)`, tüm sayısal olmayan karakterleri kaldıran bir normal ifade uygular ve **"19234564971"** döndürür. 

## <a name="example-2"></a>Örnek 2

`REPLACE ("abcdef", "cd", "GH", false)`, **"cd"** deseni değiştirir, şunun ile: **"GH"** ve bunu döndürür: **"abGHef"**.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]