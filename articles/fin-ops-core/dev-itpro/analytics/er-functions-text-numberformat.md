---
title: NUMBERFORMAT ER işlevi
description: Bu konu, NUMBERFORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 8de57d8b0a45b8b58849a24f2d8f0cde41e0ea3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746230"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER işlevi

[!include [banner](../includes/banner.md)]

`NUMBERFORMAT` işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde belirtilen sayıyı gösteren bir *dize* değeri döndürür. Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

## <a name="syntax-1"></a>Sözdizimi 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Sözdizimi 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Tamsayı* veya *Gerçek*

Biçimlendirilmesi gereken sayıyı belirten sayısal değer.

`format`: *Dize*

Biçimi temsil eden bir *dize* değeri.

`culture`: *Dize*

Biçimlendirme için kullanılacak kültürü temsil eden bir *dize* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlanmamışsa, bu işlevin çalıştırıldığı bağlam numaraları biçimlendirmek için kullanılan kültürü belirler.

## <a name="example-1"></a>Örnek 1

**TR-TR** kültürü için `NUMBERFORMAT (0.45, "p")` **"% 45.00"** ve `NUMBERFORMAT (10.45, "#")`, **"10"** döndürür.

## <a name="example-2"></a>Örnek 2

`NUMBERFORMAT (10/3, "F2", "de")`, **3,33**; `NUMBERFORMAT (10/3, "F2", "en-us")`, **3.33** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]