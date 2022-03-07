---
title: NUMBERVALUE ER işlevi
description: Bu konu, NUMBERVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561434"
---
# <a name="numbervalue-er-function"></a>NUMBERVALUE ER işlevi

[!include [banner](../includes/banner.md)]

Bu `NUMBERVALUE` işlev, belirtilen *dize* değerinden dönüştürülen *gerçek* değeri döndürür. Dönüştürme sırasında, belirtilen ondalık ve basamak gruplandırma ayırıcıları dikkate alınır.

## <a name="syntax"></a>Sözdizimi

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]