---
title: NUMBERVALUE ER işlevi
description: Bu konu, NUMBERVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916534"
---
# <a name="NUMBERVALUE">NUMBERVALUE ER işlevi</a>

[!include [banner](../includes/banner.md)]

Bu `NUMBERVALUE` işlev, belirtilen *dize* değerinden dönüştürülen *gerçek* değeri döndürür. Dönüştürme sırasında, belirtilen ondalık ve basamak gruplandırma ayırıcıları dikkate alınır.

## <a name="syntax"></a>Sözdizimi

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Bir *Gerçek* numarasına dönüştürülmesi gereken metin değeri.

`decimal separator`: Dize

Ondalık ayırıcısı. Ondalık sayının tamsayı ve kesirli kısımlarını ayırmak için kullanılır.

`digit grouping separator`: *Dize*

Basamak gruplandırma ayırıcısı. Binler ayırıcısı olarak kullanılır.

## <a name="return-values"></a>Dönüş değerleri

*Gerçek*

Sonuç sayısal değeri.

## <a name="example"></a>Örnek

`NUMBERVALUE( "1 234,56", ",", " ")`, **1234.56** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tür dönüştürme işlemleri](er-functions-category-type-conversion.md)
