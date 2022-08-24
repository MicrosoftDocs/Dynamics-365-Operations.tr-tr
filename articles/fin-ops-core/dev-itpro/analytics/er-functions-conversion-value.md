---
title: VALUE ER işlevi
description: Bu makalede, VALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: 0a47637c47ca6c947451efa1230191779401b4e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277677"
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
