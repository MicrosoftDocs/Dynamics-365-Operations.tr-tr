---
title: DATETIMEVALUE ER işlevi
description: Bu konu, DATETIMEVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 65eb16c5846b5d194361940667da14b594d7a63c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744899"
---
# <a name="datetimevalue-er-function"></a>DATETIMEVALUE ER işlevi

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE` işlev, belirli bir metin değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde tarih/saat değeri olarak gösteren bir *TarihSaat* değeri döndürür. Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

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
