---
title: REPLACE ER işlevi
description: Bu konu, REPLACE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916879"
---
# <a name="REPLACE">REPLACE ER işlevi</a>

[!include [banner](../includes/banner.md)]

`REPLACE` işlev, belirtilen metin dizesini bir bütün veya bir kısmı başka bir dizeyle değiştirildikten sonra *dize* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```
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

`regular expression flag` Bağımsız değişken **yanlışsa**, bu işlev [çeviri](er-functions-text-translate.md) gibi davranır. Belirtilen değiştirme `replacement` bağımsız değişkenindeki karakterler, bulunan karakterleri değiştirmek için kullanılır. 

## <a name="example-1"></a>Örnek 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)`, tüm sayısal olmayan karakterleri kaldıran bir normal ifade uygular ve **"19234564971"** döndürür. 

## <a name="example-2"></a>Örnek 2

`REPLACE ("abcdef", "cd", "GH", false)`, **"cd"** deseni değiştirir, şunun ile: **"GH"** ve bunu döndürür: **"abGHef"**.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)