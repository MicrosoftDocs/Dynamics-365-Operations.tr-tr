---
title: ROUNDDOWN ER işlevi
description: Bu konu, ROUNDDOWN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ac559983609d4fdb80c9ac70d84031e4a231889
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744539"
---
# <a name="rounddown-er-function"></a>ROUNDDOWN ER işlevi

[!include [banner](../includes/banner.md)]

`ROUNDDOWN` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı aşağı yuvarladıktan sonra *Gerçek* değer olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Gerçek*

Aşağı yuvarlama gereken sayısal değer.

`decimals`: *Tamsayı*

Ondalık basamak sayısını temsil eden sayısal değer.

## <a name="return-values"></a>Dönüş değerleri

*Gerçek*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlev [YUVARLA](er-functions-mathematical-round.md) işlevi gibi davranır ancak belirtilen sayıyı daima aşağı doğru (sıfıra doğru) yuvarlar.

## <a name="example-1"></a>Örnek 1

`ROUNDDOWN (1200.767, 2)` iki ondalık basamağa aşağı yuvarlar ve **1200.76** sonucunu döndürür. 

## <a name="example-2"></a>Örnek 2

`ROUNDDOWN (1700.767, -3)`, 1.000'in en yakın katına aşağı yuvarlar ve **1000** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Matematik işlevi](er-functions-category-mathematical.md)
