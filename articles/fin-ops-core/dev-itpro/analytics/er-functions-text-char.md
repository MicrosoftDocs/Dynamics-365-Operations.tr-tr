---
title: CHAR ER işlevi
description: Bu konu, CHAR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b008cf6ddf51d816a17e0fae1fa0db464adeabde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563210"
---
# <a name="char-er-function"></a>CHAR ER işlevi

[!include [banner](../includes/banner.md)]

Bu `CHAR` işlev, belirtilen Unicode sayısı tarafından başvurulan tek bir karakteri gösteren bir *dize* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
CHAR (number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Tamsayı*

Beklenen tek bir karaktere karşılık gelen sayı.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlevin döndürdüğü dize **DOSYA** biçimi üst öğesinde seçtiğiniz kodlamaya bağlıdır. Desteklenen kodlamalar listesi için bkz. [Kodlama sınıfı](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Örnek

`CHAR (255)`, **"ÿ"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]