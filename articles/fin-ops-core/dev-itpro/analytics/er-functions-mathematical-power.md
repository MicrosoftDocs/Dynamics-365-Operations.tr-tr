---
title: POWER ER işlevi
description: Bu makalede, POWER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: da3ae988b57cb5588de1e2fd8ee962b77b5534ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864702"
---
# <a name="power-er-function"></a>POWER ER işlevi

[!include [banner](../includes/banner.md)]

`POWER` işlev, belirtilen pozitif sayıyı belirtilen güce yükseltme sonucunu gösteren *gerçek* bir değer döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
POWER (number, power)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Gerçek* veya *tamsayı*

Belirtilen üsse yükseltilmiş sayısal değer.

`power`: *Gerçek* veya *tamsayı*

Belirli bir gücü temsil eden sayısal değer.

## <a name="return-values"></a>Dönüş değerleri

*Gerçek*

Sonuç sayısal değeri.

## <a name="example-1"></a>Örnek 1

`POWER (10, 2)`, **100** döndürür.

## <a name="example-2"></a>Örnek 2

`POWER (4, 0.5)`, **2** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Matematik işlevi](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]