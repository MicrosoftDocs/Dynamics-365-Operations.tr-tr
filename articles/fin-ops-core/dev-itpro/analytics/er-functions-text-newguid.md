---
title: NEWGUID ER işlevi
description: Bu konu, NEWGUID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647962"
---
# <a name="newguid-er-function"></a>NEWGUID ER işlevi

[!include [banner](../includes/banner.md)]

`NEWGUID` işlevi, yeni bir genel benzersiz tanımlayıcı (GUID) oluşturur ve bunu *[GUID](er-formula-supported-data-types-primitive.md#guid)* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
NEWGUID ()
```

## <a name="return-values"></a>Dönüş değerleri

*GUID*

Sonuç GUID değeri.

## <a name="example"></a>Örnek

`NEWGUID()` her zaman, **3afcf7ff-af10-ec11-b6e6-000d3a13209e** gibi yeni bir *GUID* değeri döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
