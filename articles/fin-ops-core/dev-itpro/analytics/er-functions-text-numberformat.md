---
title: NUMBERFORMAT ER işlevi
description: Bu konu, NUMBERFORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070564"
---
# <a name="NUMBERFORMAT">NUMBERFORMAT ER işlevi</a>

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
