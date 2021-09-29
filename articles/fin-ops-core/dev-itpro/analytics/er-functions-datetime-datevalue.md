---
title: DATEVALUE ER işlevi
description: Bu konu, DATEVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: 446f1357e54342073e73f86ef36e6467e029ebc4
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485586"
---
# <a name="datevalue-er-function"></a>DATEVALUE ER işlevi

[!include [banner](../includes/banner.md)]

`DATEVALUE` işlevi, belirli bir metin değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde tarih/saat değeri olarak gösteren bir *[Tarih](er-formula-supported-data-types-primitive.md#date)* değeri döndürür. Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](/dotnet/standard/base-types/standard-date-and-time-format-strings) ve [özel](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Sözdizimi 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Sözdizimi 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *[Dize](er-formula-supported-data-types-primitive.md#string)*

Biçimlendirilecek değeri gösteren bir metin değeri.

`format`: *Dize*

Belirli metnin biçimi. Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](/dotnet/standard/base-types/standard-date-and-time-format-strings) ve [özel](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *Dize*

Verilen metnin biçimlendirilmesi için kullanılan kültür. Desteklenen kültürler hakkında bilgi için bkz. [kültür](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Dönüş değerleri

*Date*

Sonuç tarih değeri.

## <a name="usage-notes"></a>Kullanım notları

Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlandığında, `culture` değeri çağıran bağlam tarafından tanımlanır. Örneğin, `DATEVALUE` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır. Varsayılan `culture` değeri **EN-US**'dir.

## <a name="example-1"></a>Örnek 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")`, belirtilen özel biçim ve varsayılan uygulamanın **en-US** kültürü temelinde **21 Aralık 2016** tarih değeri arasında bir değer verir.

## <a name="example-2"></a>Örnek 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")`, belirtilen özel biçime ve kültüre dayalı olarak **21Ocak 2016** Tarih değerlerini döndürür.

Bununla birlikte, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` belirtilen dizenin geçerli bir tarih olarak tanınmadığını kullanıcıya bildirmek için bir özel durum oluşturur.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
