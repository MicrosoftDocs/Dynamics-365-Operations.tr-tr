---
title: TRIM ER işlevi
description: Bu makalede, TRIM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: deadf89641771efa864e701af9dad57c5e62ea37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864673"
---
# <a name="trim-er-function"></a>TRIM ER işlevi

[!include [banner](../includes/banner.md)]

`TRIM` işlevi, sekme, satır başı, satır beslemesi ve form besleme karakterlerinin yerine tek bir boşluk karakteriyle konulduktan sonra, baştaki ve sondaki boşlukların kesildikten sonra ve sözcüklerin arasındaki birden çok boşluk kaldırıldığında bir *Dize* değeri olarak belirtilen metin dizesini döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
TRIM (text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

*Dize* türünün veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

Bazı durumlarda, baştaki ve sondaki boşlukları kesmek ve belirtilen metin için biçimlendirmeyi saklamayı tercih etmek isteyebilirsiniz. Örneğin, bu metin çok satırlı metin kutusuna girilebilecek bir adresi temsil ettiğinde ve satır besleme ve satır sonu biçimlendirmesi içerebilir. Bu durumda, şu ifadeyi kullanın: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)`. Bu ifadede `text`, belirtilen metin dizesine başvuran bağımsız değişkendir.

## <a name="example-1"></a>Örnek 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")`, **"Örnek metin"** döndürür.

## <a name="example-2"></a>Örnek 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` **"Sample text"** ifadesini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)

[REPLACE ER işlevi](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
