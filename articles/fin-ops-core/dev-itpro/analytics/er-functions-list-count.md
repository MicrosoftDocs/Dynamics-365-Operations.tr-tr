---
title: COUNT ER işlevi
description: Bu konu, COUNT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
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
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746639"
---
# <a name="count-er-function"></a>COUNT ER işlevi

[!include [banner](../includes/banner.md)]

Bu `COUNT` işlev, liste boş değilse, belirtilen listedeki kayıt sayısını gösteren bir *tamsayı* değer döndürür. Liste boşsa, bu işlev **0** (sıfır) döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
COUNT (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Tamsayı*

Sonuç sayısal değeri.

## <a name="example"></a>Örnek

`COUNT (SPLIT("abcd" , 3))`, **2** döndürür, çünkü bu örnekte kullanılan `SPLIT` işlev iki kayıttan oluşan bir liste oluşturur.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]