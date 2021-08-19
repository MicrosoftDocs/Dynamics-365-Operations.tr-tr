---
title: EMPTYRECORD ER işlevi
description: Bu konu, EMPTYRECORD Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 5aea5533f5d0530cdc9ccae0b0b8355245599bc77e37fde87a13e8e5a1443695
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725198"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD ER işlevi

[!include [banner](../includes/banner.md)]

`EMPTYRECORD` işlev, belirtilen kayıt listesi veya kayıtla aynı yapıya sahip bir boş *Konteyner (kayıt)* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi* veya *konteyner (kayıt)*

*Kayıt listesi* veya *konteyner (kayıt)* türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner (kayıt)*

Sonuç kayıt değeri.

## <a name="usage-notes"></a>Kullanım notları

> [!NOTE] 
> Boş kayıt, tüm alanlarda boş değeri bulunan kayıttır. Boş değer sayılar için **0** (sıfır), dizeler için boş bir dize vb.'dir.

## <a name="example"></a>Örnek

`EMPTYRECORD (SPLIT ("abc", 1))`, `SPLIT` işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir kayıt döndürür. Daha fazla bilgi için bkz. [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Kayıt işlevleri](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]