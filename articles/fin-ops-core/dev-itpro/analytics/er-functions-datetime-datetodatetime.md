---
title: DATETODATETIME ER işlevi
description: Bu makalede, DATETODATETIME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 30fe75c7fd68edfff3e3778192723792d0f342ab
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287323"
---
# <a name="datetodatetime-er-function"></a>DATETODATETIME ER işlevi

[!include [banner](../includes/banner.md)]

`DATETODATETIME` işlev, Eşgüdümlü evrensel saatdeki (Greenwich saati \[GMT\]) belirli bir tarih değerinden bir tarih/saat değerine dönüştürülmüş bir *tarih saat* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Bağımsız değişkenler

`date`: *Tarih*

Değiştirilecek tarihi gösteren bir tarih değeri.

## <a name="return-values"></a>Dönüş değerleri

*DateTime*

Sonuç tarih/saat değeri.

## <a name="example-1"></a>Örnek 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')`, 24 Aralık 2015 olan geçerli Microsoft Dynamics 365 Finance oturumunun tarihini **12/24/2015 12:00:00** olarak döndürür. Bu örnekte, **CompInfo** **finans ve operasyon/Tablo** türünde bir elektronik raporlama (ER) veri kaynağıdır ve CompanyInfo tablosuna başvurur.

## <a name="example-2"></a>Örnek 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` **11/12/2019 12:00:00** değerini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
