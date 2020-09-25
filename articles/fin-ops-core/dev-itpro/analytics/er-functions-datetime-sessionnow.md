---
title: SESSIONNOW ER işlevi
description: Bu konu, SESSIONNOW Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 00c41564b18eed477e1cefb0bc3bb2bca3fa6fdd
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745477"
---
# <a name="sessionnow-er-function"></a>SESSIONNOW ER işlevi

[!include [banner](../includes/banner.md)]

`SESSIONNOW` işlevi, geçerli uygulama oturumu tarih ve saatini temsil eden bir *TarihSaat* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
SESSIONNOW ()
```

## <a name="return-values"></a>Dönüş değerleri

*DateTime*

Sonuç tarih/saat değeri.

## <a name="example"></a>Örnek

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarih/saat değerini (24 Aralık 2015) döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)
