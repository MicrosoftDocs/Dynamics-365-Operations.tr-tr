---
title: ROUND ER işlevi
description: Bu konu, ROUND Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041619"
---
# <a name="ROUND">ROUND ER işlevi</a>

[!include [banner](../includes/banner.md)]

`ROUND` işlev, belirtilen sayıyı, ondalık basamağındaki sayısı yuvarladıktan sonra *Gerçek* değer olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Gerçek*

Yuvarlama gereken sayısal değer.

`decimals`: *Tamsayı*

Ondalık basamak sayısını temsil eden sayısal değer.

## <a name="return-values"></a>Dönüş değerleri

*Gerçek*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Ondalık parametresinin değeri 0'dan (sıfır) büyükse, belirtilen sayı birçok `decimals` basamağa yuvarlanır.

`decimals` bağımsız değişkeni değeri **0** (sıfır) ise, belirtilen sayı en yakın tamsayıya yuvarlanır.

`decimals` bağımsız değişkeni değeri 0'dan (sıfır) küçükse, belirtilen sayı ondalık basamağın soluna yuvarlanır.

## <a name="example-1"></a>Örnek 1

`ROUND (1200.767, 2)` iki ondalık basamağa yuvarlar ve **1200.77** sonucunu döndürür.

## <a name="example-2"></a>Örnek 2

`ROUND (1200.767, -3)`, 1.000'in en yakın katına yuvarlar ve **1000** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Matematik işlevi](er-functions-category-mathematical.md)
