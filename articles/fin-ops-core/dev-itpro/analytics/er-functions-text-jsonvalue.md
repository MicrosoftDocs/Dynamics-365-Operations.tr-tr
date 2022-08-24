---
title: JSONVALUE ER işlevi
description: Bu makalede, JSONVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 10/25/2021
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
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267995"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER işlevi

[!include [banner](../includes/banner.md)]

`JSONVALUE` işlevi, verileri, belirtilen koda göre skaler bir değer çıkarmak için belirtilen yolla erişilen JavaScript Nesne Gösterimi (JSON) biçiminde ayrıştırın. Sonra da bir *dize* değeri olarak ayıklanan skalar değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Dize*

JSON verileri içeren *Dize* türünün veri kaynağının geçerli yolu.

`path`: *Dize*

JSON verileri sklar değeri tanımlayıcısı. İlgili JSON düğümlerinin adlarını ayırmak için eğik çizgi (/) kullanın. Bir JSON dizisindeki belirli bir değerin dizinini belirtmek için köşeli ayraç (\[\]) gösterimini kullanın. Bu dizin için sıfır tabanlı numaralandırmanın kullanıldığını unutmayın.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example-1"></a>Örnek 1

**JsonField** veri kaynağı, aşağıdaki veriyi JSON biçiminde içerir: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. Bu durumda `JSONVALUE (JsonField, "BuildNumber")` ifadesi, *dize* veri türünün şu değerini döndürür: **"7.3.1234.1".**

## <a name="example-2"></a>Örnek 2

*Hesaplanmış alan* türünün **JsonField** veri kaynağı aşağıdaki ifadeyi içerir: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Bu ifade, , aşağıdaki verileri JSON biçiminde gösteren bir [*Dize*](er-formula-supported-data-types-primitive.md#string) değeri döndürmek için yapılandırılmıştır.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

Bu durumda `JSONVALUE(json, "workers/[1]/emails/[0]")` ifadesi, *Dize* veri türünün şu değerini döndürür: `JohnS@Contoso.com`

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
