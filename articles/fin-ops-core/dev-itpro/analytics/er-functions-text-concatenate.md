---
title: CONCATENATE ER işlevi
description: Bu konu, CONCATENATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569617"
---
# <a name="concatenate-er-function"></a>CONCATENATE ER işlevi

[!include [banner](../includes/banner.md)]

Bu `CONCATENATE` işlev, bir dizeye katıldıktan sonra, belirtilen tüm metin dizelerini bir *dize* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Bağımsız değişkenler

`text 1`: *Dize*

*Dize* veri türünün veri kaynağına yönelik referans. Bu bağımsız değişken gereklidir.

`text N`: *Dize*

*Dize* veri türünün veri kaynağına yönelik referans. Bu ek bağımsız değişkenler isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`CONCATENATE ("abc", "def")`, **"abcdef"** döndürür.

## <a name="usage-notes"></a>Kullanım notları

`"abc" & "def"` ifadesi ayrıca **"abcdef"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]