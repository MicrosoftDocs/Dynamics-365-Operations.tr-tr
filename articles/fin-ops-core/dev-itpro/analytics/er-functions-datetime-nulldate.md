---
title: NULLDATE ER işlevi
description: Bu konu, NULLDATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 24a295a6ad8aca7718e60dd351248c9fbfdafee8
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042332"
---
# <a name="NULLDATE">NULLDATE ER işlevi</a>

[!include [banner](../includes/banner.md)]

`NULLDATE` işlev, **boş** tarihi temsil eden bir *tarih* değeri döndürür (1 Ocak, 1900).

## <a name="syntax"></a>Sözdizimi

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Dönüş değerleri

*Tarih*

Sonuç tarih değeri.

## <a name="example-1"></a>Örnek 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` belirtilen özel biçime dayalı olarak, 1 Ocak 1900 arasındaki **boş** tarihi **"1900-01-01"** olarak döndürür.

## <a name="example-2"></a>Örnek 2

`IF( Invoice.DocumentDate = NULLDATE(), true, false)`, **Documentdate** alanının değeri **boş** tarihine eşit olduğunda ifade **doğru** değerini döndürür. Bu örnekte, **Fatura** **Finance/Operations kyıtları** türünde bir elektronik raporlama (ER) veri kaynağıdır ve CustInvoiceJour tablosuna referans verir.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)
