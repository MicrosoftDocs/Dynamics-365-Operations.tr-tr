---
title: NEWGUID ER işlevi
description: Bu makalede, NEWGUID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861830"
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
