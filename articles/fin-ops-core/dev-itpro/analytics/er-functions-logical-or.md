---
title: OR ER işlevi
description: Bu konu, OR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686990"
---
# <a name="or-er-function"></a>OR ER işlevi

[!include [banner](../includes/banner.md)]

Belirtilen koşulların tümü yanlış ise, `OR` işlev **yanlış** *Boole* değerini döndürür. Belirtilen koşullardan biri doğruysa bu işlev **DOĞRU** *Boole* değerini döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Bağımsız değişkenler

`condition 1`: *Boole*

Test işlem uygulanacak geçerli bir koşullu ifade. Bu bağımsız değişken gereklidir.

`condition N`: *Boole*

Test işlem uygulanacak geçerli bir koşullu ifade. Bu ek bağımsız değişkenler isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Boole*

Sonuç *Boole* değeri.

## <a name="example"></a>Örnek

`OR (1=2, "a"="a")`, **DOĞRU** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)
