---
title: VALUE ER işlevi
description: Bu konu, VALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752592"
---
# <a name="value-er-function"></a>VALUE ER işlevi

[!include [banner](../includes/banner.md)]

Bu `VALUE` işlevi, belirtilen dizeden dönüştürülen *gerçek* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
VALUE (text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Bir sayısal değere dönüştürülmesi gereken dize değeri.

## <a name="return-values"></a>Dönüş değerleri

*Gerçek*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Virgül ve nokta karakterleri (.) ondalık ayırıcı olarak kabul edilir ve önde gelen bir tire (-), bir eksi işareti olarak kullanılır. Belirtilen dizenin sayısal olmayan karakterler içermesi durumunda bir özel durum oluşturur.

## <a name="example-1"></a>Örnek 1

`VALUE ("1 234,56")`, özel durum oluşturur:

## <a name="example-2"></a>Örnek 2

`VALUE ("1234,56")`, **1234.56** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tür dönüştürme işlemleri](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]