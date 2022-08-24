---
title: NEWGUID ER işlevi
description: Bu makalede, NEWGUID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274787"
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
