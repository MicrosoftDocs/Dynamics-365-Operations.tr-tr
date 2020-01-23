---
title: GUIDVALUE ER işlevi
description: Bu konu, GUIDVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: be5e8e7625d0226c9eb59efd3217fce7b8eba086
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915706"
---
# <a name="GUIDVALUE">GUIDVALUE ER işlevi</a>

[!include [banner](../includes/banner.md)]

`GUIDVALUE` işlevi, belirtilen *Dize* veri türündeki girişi *GUID* veri türünde bir veri öğesine dönüştürür.

## <a name="syntax"></a>Sözdizimi

```
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
