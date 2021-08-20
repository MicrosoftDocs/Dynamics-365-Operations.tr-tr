---
title: STRINGJOIN ER işlevi
description: Bu konu, STRINGJOIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 651cc261e6a33b1a824feb94afa767e439196e249bb13b0fc4886dc72bfdd184
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776110"
---
# <a name="stringjoin-er-function"></a>STRINGJOIN ER işlevi

[!include [banner](../includes/banner.md)]

`STRINGJOIN` işlevi, belirtilen listedeki belirtilen alanın art arda eklenmiş değerlerinden oluşan bir *dize* değeri döndürür. Değerler belirtilen sınırlayıcı ile ayrılır.

## <a name="syntax"></a>Sözdizimi

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`field`: *Alan*

*Dize* veri alanının geçerli yolu belirtilen listeyi yazın.

`delimiter`: *Dize*

Alt dizeleri ayırmak için kullanılan sınırlayıcı.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`SPLIT("abc" , 1)` veri kaynağı **DS** olarak girerseniz, ifade `STRINGJOIN (DS, DS.Value, "-")` **a-b-c** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]