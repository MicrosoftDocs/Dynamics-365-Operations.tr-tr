---
title: TRIM ER işlevi
description: Bu konu, TRIM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 816f6d6623bb778c9186d294c9b67db7edddd671
ms.sourcegitcommit: 753714ac0dabc4b7ce91509757cd19f7be4a4793
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367804"
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
