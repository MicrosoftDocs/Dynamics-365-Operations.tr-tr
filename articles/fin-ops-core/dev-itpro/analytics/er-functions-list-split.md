---
title: SPLIT ER işlevi
description: Bu makalede, SPLIT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 2acd93b645121b577d516d3ce29a3d05069b8de9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906843"
---
# <a name="split-er-function"></a>SPLIT ER işlevi

[!include [banner](../includes/banner.md)]

`SPLIT` işlev, belirtilen girdi dizesini alt dizelere böler ve sonucu yeni bir *kayıt listesi* değeri olarak döndürür.

## <a name="syntax-1"></a>Sözdizimi 1

```vb
SPLIT (input, length)
```

Bu söz dizimi, belirtilen giriş dizesini her biri belirli uzunlukta alt dizelere bölün.

## <a name="syntax-2"></a>Sözdizimi 2

```vb
SPLIT (input, delimiter)
```

Bu söz dizimi belirtilen giriş dizesini belirli sınırlayıcıya dayanarak alt dizelere bölün.

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Dize*

Bölünecek metin

`length`: *Tamsayı*

Tek bir alt dizenin maksimum uzunluğu.

`delimiter`: *Dize*

Alt dizeleri ayırmak için kullanılan sınırlayıcı.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Döndürülen listenin kayıt yapısı, *dize* türünün **değer** alanından oluşur. İade edilen her kayıt bu alanda oluşturulan alt dizeleri içerir.

`delimiter` bağımsız değişkeni boşsa, bir kayıt içeren yeni bir liste döner; kayıtta giriş metnini içeren *DİZE* **değer** alanı vardır. Bu alan giriş metnini içerir.

`input` bağımsız değişkeni boşsa, yeni boş bir liste döner. `input` veya `delimiter` bağımsız değişkeni (boş) belirtilmezse, bir uygulama özel durum oluşturulur.

## <a name="example-1"></a>Örnek 1

`SPLIT ("abcd", 3)`, *Dize* türünün **Değer** alanına sahip iki kaydı içeren yeni bir listeyi döndürür. İlk kayıttaki **Değer** alanı **"abc"** metnini içeriyor ve ikinci kayıttaki **Değer** alanı **"d"** metnini içeriyorsa.

## <a name="example-2"></a>Örnek 2

`SPLIT ("XAb aBy", "aB")`, *Dize* türünün **Değer** alanına sahip üç kaydı içeren yeni bir listeyi döndürür. İlk kayıttaki **Değer** alanı, **"X"** metni, ikinci kayıttaki **Değer** alanı **"&nbsp;"** metni, üçüncü kayıttaki **Değer** alanı **"y"** metni içerir. 

## <a name="example-3"></a>Örnek 3

Belirtilen giriş dizesinin bağımsız öğelerine erişmek için [INDEX](er-functions-list-index.md) fonksiyonunu kullanabilirsiniz. **Hesaplanmış alan** türüne ait **MyList** veri kaynağını girerseniz ve bunun için `SPLIT("abc", 1)` ifadesini yapılandırırsanız, `INDEX(MyList,2).Value` ifadesi **"b"** metnini döndürür.

## <a name="example-4"></a>Örnek 4

Belirtilen giriş dizesinin bağımsız öğelerine erişmek için [ENUMERATE](er-functions-list-enumerate.md) fonksiyonunu da kullanabilirsiniz. Önce **Hesaplanan alan** türünün **MyList** veri kaynağını girerseniz ve bunun için `SPLIT("abc", 1)` ifadesini yapılandırırsanız ve ardından **Hesaplanan alan** türünün **EnumeratedList** veri kaynağını girip bunu `ENUMERATE(MyList)` ifadesi için yapılandırırsanız `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` ifadesi **"b"** metnini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
