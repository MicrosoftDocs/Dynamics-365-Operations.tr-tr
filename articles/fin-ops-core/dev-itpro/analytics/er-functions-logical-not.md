---
title: NOT ER işlevi
description: Bu konu, NOT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: af588c3714069040fa339d3121e6eb404b9be979
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744659"
---
# <a name="not-er-function"></a>NOT ER işlevi

[!include [banner](../includes/banner.md)]

`NOT` işlev, belirtilen koşulun ters çevrilmiş mantıksal değerini bir *Boole* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
NOT (condition)
```

## <a name="arguments"></a>Bağımsız değişkenler

`condition`: *Boole*

Ters işlem uygulanacak geçerli bir koşullu ifade.

## <a name="return-values"></a>Dönüş değerleri

*Boole*

Sonuç *Boole* değeri.

## <a name="example"></a>Örnek

`NOT (TRUE)`, **YANLIŞ** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)
