---
title: OR ER işlevi
description: Bu makalede, OR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: d2783b5aff34e6ab4b5bde5dfe39e92d20892634
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892965"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]