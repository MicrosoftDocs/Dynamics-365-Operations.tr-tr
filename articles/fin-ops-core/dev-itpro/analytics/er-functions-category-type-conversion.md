---
title: Tür dönüştürme kategorisindeki ER işlevlerinin listesi
description: Bu makalede, Elektronik raporlama (ER) uygulamasında desteklenen dönüştürme işlevleri hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 00fe8c5bce40a59580509a719212f163238815be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292631"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Tür dönüştürme kategorisindeki ER işlevlerinin listesi

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) tür dönüştürme işlevleri, değerleri türler arasında dönüştürmek için kullanılabilir. Bu makale, bu işlevlerin özetini sunmaktadır.

## <a name="type-conversion-functions"></a>Tür dönüştürme işlevleri

| İşlev | Tanım |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Bu işlevi, belirtilen dizeyi temsil eden bir *Int64* değeri döndürür. |
| [IntValue](er-functions-conversion-intvalue.md)       | Bu işlevi, belirtilen dizeyi temsil eden bir *Int* değeri döndürür. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Bu işlev, belirtilen *dize* değerinden dönüştürülen *gerçek* değeri döndürür. Dönüştürme sırasında, belirtilen ondalık ve basamak gruplandırma ayırıcıları dikkate alınır. |
| [Değer](er-functions-conversion-value.md)             | Bu işlev, belirtilen *dize* değerinden dönüştürülen *gerçek* değeri döndürür. |

## <a name="type-conversion-functions-in-the-container-category"></a>Konteyner kategorisindeki tür dönüştürme işlevleri

Aşağıdaki tabloda [konteyner](er-functions-category-container.md) kategorisinde tür dönüştürme işlevleri açıklanmıştır.

| İşlev | Tanım |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Bu işlev, belirtilen *Dize* veri türündeki girişi *Konteyner* türünde bir veri öğesine dönüştürür. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Tarih ve zaman kategorisindeki tür dönüştürme işlevleri

Aşağıdaki tabloda [tarih ve saat kategorisinde](er-functions-category-datetime.md) tür dönüştürme işlevleri açıklanmıştır.

| İşlev | Tanım |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Bu işlev, belirli bir *Dize* değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde tarih/saat değeri olarak gösteren bir *TarihSaat* değeri döndürür. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Bu işlev, Eşgüdümlü evrensel saatdeki (Greenwich saati \[GMT\]) belirli bir *Tarih* değerinden bir tarih/saat değerine dönüştürülmüş bir *tarih saat* değeri döndürür. |
| [DateValue](er-functions-datetime-datevalue.md)           | Bu işlev, belirli bir *Dize* değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde tarih değeri olarak gösteren bir *Tarih* değeri döndürür. |

## <a name="type-conversion-functions-in-the-list-category"></a>Liste kategorisindeki tür dönüştürme işlevleri

Aşağıdaki tabloda [liste kategorisinde](er-functions-category-list.md) tür dönüştürme işlevleri açıklanmıştır.

| İşlev | Tanım |
|----------|-------------|
| [Liste](er-functions-list-list.md)                 | Bu işlevi, *konteyner (kayıt)* türünün belirtilen bağımsız değişkenlerden oluşturulmuş yeni listeden oluşan yeni bir *kayıt listesi* değeri döndürür. |
| [ListOfFields](er-functions-list-listoffields.md) | Bu işlev, *numaralandırmanın* veya *konteyner (kayıt)* türünün belirli bağımsız değişkeninin yapısına göre oluşturulan bir *kayıt listesi* değeri döndürür. |
| [Böl](er-functions-list-split.md)               | Bu işlev, belirtilen *Dize* değeri alt dizelere böler ve sonucu yeni bir *kayıt listesi* değeri olarak döndürür. |
| [StringJoin](er-functions-list-stringjoin.md)     | Bu işlevi, belirtilen *Kayıt listesi* değerindeki belirtilen alanın art arda eklenmiş değerlerinden oluşan bir *Dize* değeri döndürür. Değerler belirtilen sınırlayıcı ile ayrılır. |

## <a name="type-conversion-functions-in-the-text-category"></a>Metin kategorisindeki tür dönüştürme işlevleri

Aşağıdaki tabloda [metin kategorisinde](er-functions-category-text.md) tür dönüştürme işlevleri açıklanmıştır.

| İşlev | Tanım |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Bu işlev, belirtilen Unicode sayısı tarafından başvurulan tek bir karakteri gösteren bir *dize* değeri döndürür. |
| [GuidValue](er-functions-text-guidvalue.md)       | Bu işlevi, belirtilen *Dize* veri türündeki girişi *GUID* veri türünde bir veri öğesine dönüştürür. |
| [NumberFormat](er-functions-text-numberformat.md) | Bu işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde belirtilen sayıyı gösteren bir *dize* değeri döndürür. |
| [QrCode](er-functions-text-qrcode.md)             | Bu işlev, belirtilen dizgi için hızlı yanıt kodu (QR kodu) görüntüsünü ikili biçimde gösteren bir *konteyner* değeri döndürür. |
| [Metin](er-functions-text-text.md)                 | Bu işlevi, belirtilen giriş geçerli uygulama örneğinin sunucu yerel ayarlarına göre biçimlendirilmiş bir metin dizesine çevrildikten sonra bleirtilen sayıyı *dize* değeri olarak döndürür. |

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Elektronik raporlamada formül dili](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
