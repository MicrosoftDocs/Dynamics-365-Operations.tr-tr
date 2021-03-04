---
title: POWER ER işlevi
description: Bu konu, POWER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683341"
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