---
title: CONCATENATE ER işlevi
description: Bu makalede, CONCATENATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 230bbbac5df7824c3ef7d0550cc45dbf6c374858
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267299"
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
