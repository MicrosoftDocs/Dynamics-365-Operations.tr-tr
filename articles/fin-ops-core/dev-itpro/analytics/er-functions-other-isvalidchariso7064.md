---
title: ISVALIDCHARACTERISO7064 ER işlevi
description: Bu konu, ISVALIDCHARACTERISO7064 Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21962952bb3bdd016831dc5e196af27c69ecc6db
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744083"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ISVALIDCHARACTERISO7064 ER işlevi

[!include [banner](../includes/banner.md)]

`ISVALIDCHARACTERISO7064` işlevi, belirtilen dize, geçerli bir uluslararası banka hesap numarasını (IBAN) temsil ediyorsa, **DOĞRU** *boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Bir IBAN'ı temsil eden metin değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")`, **DOĞRU** döndürür. 

`ISVALIDCHARACTERISO7064 ("AT61")`, **YANLIŞ** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)
