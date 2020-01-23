---
title: STRINGJOIN ER işlevi
description: Bu konu, STRINGJOIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 99d50313f8097d43b820ffc1c36eef0097e7ec55
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917201"
---
# <a name="STRINGJOIN">STRINGJOIN ER işlevi</a>

[!include [banner](../includes/banner.md)]

`STRINGJOIN` işlevi, belirtilen listedeki belirtilen alanın art arda eklenmiş değerlerinden oluşan bir *dize* değeri döndürür. Değerler belirtilen sınırlayıcı ile ayrılır.

## <a name="syntax"></a>Sözdizimi

```
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
