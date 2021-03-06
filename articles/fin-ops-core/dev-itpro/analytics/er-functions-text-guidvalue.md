---
title: GUIDVALUE ER işlevi
description: Bu konu, GUIDVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: ec8222708b999a17794a396b5bf807dab037799d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746399"
---
# <a name="guidvalue-er-function"></a>GUIDVALUE ER işlevi

[!include [banner](../includes/banner.md)]

`GUIDVALUE` işlevi, belirtilen *Dize* veri türündeki girişi *GUID* veri türünde bir veri öğesine dönüştürür.

## <a name="syntax"></a>Sözdizimi

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Dize*

*Dize* türünün veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*GUID*

Sonuçta elde edilen genel benzersiz tanımlayıcı (GUID) değeri.

## <a name="usage-notes"></a>Kullanım notları

Ters yönde dönüştürme yapmak için (diğer bir deyişle, *GUID* veri türünün belirtilen girişini *Dize* veri türünün veri öğesine dönüştürmek için), [TEXT()](er-functions-text-text.md) işlevini kullanabilirsiniz.

## <a name="example"></a>Örnek

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:

- `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` ifadeyi içeren *hesaplanmış alan* türünün **myID** bir veri kaynağı
- UserInfo tablosuna başvuran *Tablo kayıtları* türünün **Kullanıcılar** veri kaynağı

Daha sonra, bir *GUID* veri türünün **ObjectID** alanı ile UserInfo tablosunu filtrelemek için `FILTER (Users, Users.objectId = myID)` gibi bir ifade kullanabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]