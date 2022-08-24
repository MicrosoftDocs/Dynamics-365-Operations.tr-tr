---
title: TABLENAME2ID ER işlevi
description: Bu makalede, TABLENAME2ID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: fe7ed336f2264e15e0a8a7305e1bcebb75b2cd07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268071"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER işlevi

[!include [banner](../includes/banner.md)]

Bu `TABLENAME2ID` işlevi, belirtilen tablo için tablo kodunun sayısal gösterimini *tamsayı* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Geçerli bir tablo adını gösteren bir metin değeri.

## <a name="return-values"></a>Dönüş değerleri

*Tamsayı*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlevin yürütülmesi, aynı şirket adı kullanılsa bile farklı Microsoft Dynamics 365 Finance örneklerinde farklı sonuçlar elde edebilir.

## <a name="example"></a>Örnek

`TABLENAME2ID ("Intrastat")`, **1510** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
