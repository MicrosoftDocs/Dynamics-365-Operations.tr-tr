---
title: DATETIMEFORMAT ER işlevi
description: Bu konu, DATETIMEFORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 01/04/2021
ms.topic: article
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
ms.openlocfilehash: 8044f81ee59af4a11bfab38525afdac5a46acd2c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891269"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT ER işlevi

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` işlev, belirli bir tarih/saat değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde metin olarak gösteren bir *dize* değeri döndürür. Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](/dotnet/standard/base-types/standard-date-and-time-format-strings) ve [özel](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Sözdizimi 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Sözdizimi 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Bağımsız değişkenler

`datetime`: *TarihSaat*

Biçimlendirilecek tarihi ve saati gösteren tarih/saat değeri.

`format`: *Dize*

Çıkış dizesinin biçimi.

> [!NOTE]
> Standart biçim veya özel biçim kullanırken biçim dizesi büyük/küçük harfe duyarlıdır. Örneğin, [standart](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" biçim tanımlayıcısı kısa tarih modelini kullanarak tarihi döndürürken standart "D" biçim tanımlayıcısı uzun tarih modelini kullanarak tarihi döndürür. Ek olarak, [özel](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" biçim tanımlayıcısı 1 ile 12 arasındaki ayları döndürürken özel "m" biçim tanımlayıcısı 0 ile 59 arasındaki dakikaları döndürür.

`culture`: *Dize*

Biçimlendirme için kullanılacak kültür.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç dize değeri.

## <a name="usage-notes"></a>Kullanım notları

Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlanmamışsa `culture` değeri, çağıran bağlam tarafından tanımlanır. Örneğin, `DATETIMEFORMAT` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır. Varsayılan `culture` değeri **EN-US**'dir.

`DATETIMEFORMAT` işlev verilen bir tarih/saat değerini dönüştürdüğünde, işlevin bağlamında çağrıldığı ER biçimini çalıştıran uygulama kullanıcısının saat dilimi ayarını dikkate alır.

## <a name="example-1"></a>Örnek 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarih/saat değerini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.

## <a name="example-2"></a>Örnek 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarih/saat değerini (24 Aralık 2015) döndürür.

## <a name="example-3"></a>Örnek 3

İşlev, **Dil ve ülke/bölge tercihleri** bölümünde saat dilimi değeri **(GMT-08:00) Pasifik Saati (ABD ve Kanada)** olan bir uygulama kullanıcı tarafından başlatılan işlem sırasında çağrıldığında `DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")`, **2019-11-12T08:00:00.0000000-08:00** dize değerini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]