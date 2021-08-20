---
title: DATETIMEVALUE ER işlevi
description: Bu konu, DATETIMEVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 711889e23e85b05c5e4c5ab904ec12ceb0bbb4da1f17d1c994adda1eec8ccb74
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776182"
---
# <a name="datetimevalue-er-function"></a>DATETIMEVALUE ER işlevi

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE` işlev, belirli bir metin değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde tarih/saat değeri olarak gösteren bir *TarihSaat* değeri döndürür. Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](/dotnet/standard/base-types/standard-date-and-time-format-strings) ve [özel](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Sözdizimi 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Sözdizimi 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Biçimlendirilecek değeri gösteren bir metin değeri.

`format`: *Dize*

Belirli metnin biçimi.

`culture`: *Dize*

Verilen metnin biçimlendirilmesi için kullanılan kültür.

## <a name="return-values"></a>Dönüş değerleri

*DateTime*

Sonuç tarih/saat değeri.

## <a name="usage-notes"></a>Kullanım notları

Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlandığında, `culture` değeri çağıran bağlam tarafından tanımlanır. Örneğin, `DATETIMEVALUE` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır. Varsayılan `culture` değeri **EN-US**'dir.

## <a name="example-1"></a>Örnek 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")`, belirtilen özel biçim ve varsayılan uygulamanın **en-US** kültürü temelinde **2:55:00 ile 21 Aralık 2016** arasında bir değer verir.

## <a name="example-2"></a>Örnek 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` belirtilen özel biçim ve kültür temelinde **2:55:00 Ile21 Aralık 2016** arasında bir değer döndürür.

Bununla birlikte, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` belirtilen dizenin geçerli bir tarih/saat olarak tanınmadığını kullanıcıya bildirmek için bir özel durum oluşturur.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]