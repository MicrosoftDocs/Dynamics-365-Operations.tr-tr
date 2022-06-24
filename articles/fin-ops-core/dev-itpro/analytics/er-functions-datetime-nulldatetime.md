---
title: NULLDATETIME ER işlevi
description: Bu makalede, NULLDATETIME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 3e8447d4f05ee8394842b9b07d14d1c054834bb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867686"
---
# <a name="nulldatetime-er-function"></a>NULLDATETIME ER işlevi

[!include [banner](../includes/banner.md)]

`NULLDATETIME` işlev,eşgüdümlü evrensel saat (Greenwich Saati \[GMT\]) içinde **boş** tarih/zaman değerini (1 Ocak, 1900) gösteren bir *tarih saat* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Dönüş değerleri

*DateTime*

Sonuç tarih/saat değeri.

## <a name="example"></a>Örnek

`DATETIMEFORMAT( NULLDATETIME(), "O")`, Saat dilimi değerine sahip bir uygulama kullanıcısı tarafından başlatılan bir işlem sırasında çağrıldığında **1900-01-01T 00:00:00.0000000+00:00** dize değerini döndürür, **dil ve ülke/bölge tercihleri** bölümünde **Eşgüdümlü Evrensel Saat** (GMT).

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]