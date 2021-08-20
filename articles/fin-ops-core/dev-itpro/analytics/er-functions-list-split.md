---
title: SPLIT ER işlevi
description: Bu konu, SPLIT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 4a42b0c7cfa2a8d3dcb7448224c9e88a48276f7d8cdbcce484383a778b8275a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757333"
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
