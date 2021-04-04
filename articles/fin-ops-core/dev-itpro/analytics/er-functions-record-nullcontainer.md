---
title: NULLCONTAINER ER işlevi
description: Bu konu, NULLCONTAINER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: d08a4a12d2b142744d3f35c6f1088ec25158c97c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563234"
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