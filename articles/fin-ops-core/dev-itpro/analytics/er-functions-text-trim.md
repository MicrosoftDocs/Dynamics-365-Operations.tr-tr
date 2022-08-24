---
title: TRIM ER işlevi
description: Bu makalede, TRIM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273113"
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
