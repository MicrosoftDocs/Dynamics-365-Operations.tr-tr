---
title: NULLCONTAINER ER işlevi
description: Bu makalede, NULLCONTAINER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: 8efa4cce3bda1707eff052e882b74e3da9542353
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291779"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER ER işlevi

[!include [banner](../includes/banner.md)]

`NULLCONTAINER` işlev, belirtilen kayıt listesi veya kayıtla aynı yapıya sahip bir boş *Konteyner (kayıt)* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi* veya *konteyner (kayıt)*

*Kayıt listesi* veya *konteyner (kayıt)* türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner (kayıt)*

Sonuç kayıt değeri.

## <a name="usage-notes"></a>Kullanım notları

> [!NOTE] 
> Bu işlev artık kullanılmamaktadır. Bunun yerine `EMPTYRECORD` işlevi kullanın. Daha fazla bilgi için bkz. [EMPTYRECORD](er-functions-record-emptyrecord.md).

## <a name="example"></a>Örnek

`NULLCONTAINER (SPLIT ("abc", 1))`, `SPLIT` işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir kayıt döndürür. Daha fazla bilgi için bkz. [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Kayıt işlevleri](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
