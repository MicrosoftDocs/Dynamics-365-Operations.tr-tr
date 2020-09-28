---
title: JSONVALUE ER işlevi
description: Bu konu, JSONVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 985a7e4f46756e595580d77ac904c883c305b04a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743819"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER işlevi

[!include [banner](../includes/banner.md)]

`JSONVALUE` işlevi, verileri, belirtilen koda göre skaler bir değer çıkarmak için belirtilen yolla erişilen JavaScript Nesne Gösterimi (JSON) biçiminde ayrıştırın. Sonra da bir *dize* değeri olarak ayıklanan skalar değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Dize*

JSON verileri içeren *Dize* türünün veri kaynağının geçerli yolu.

`path`: *Dize*

JSON verileri sklar değeri tanımlayıcısı.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

**JsonField** veri kaynağı, aşağıdaki veriyi JSON biçiminde içerir: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. Bu durumda `JSONVALUE (JsonField, "BuildNumber")` ifadesi, *dize* veri türünün şu değerini döndürür: **"7.3.1234.1".**

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)
