---
title: EMPTYRECORD ER işlevi
description: Bu konu, EMPTYRECORD Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 2e46fcef3d53483b782ac39a0661fc0edc8d861c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743962"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD ER işlevi

[!include [banner](../includes/banner.md)]

`EMPTYRECORD` işlev, belirtilen kayıt listesi veya kayıtla aynı yapıya sahip bir boş *Konteyner (kayıt)* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi* veya *konteyner (kayıt)*

*Kayıt listesi* veya *konteyner (kayıt)* türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner (kayıt)*

Sonuç kayıt değeri.

## <a name="usage-notes"></a>Kullanım notları

> [!NOTE] 
> Boş kayıt, tüm alanlarda boş değeri bulunan kayıttır. Boş değer sayılar için **0** (sıfır), dizeler için boş bir dize vb.'dir.

## <a name="example"></a>Örnek

`EMPTYRECORD (SPLIT ("abc", 1))`, `SPLIT` işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir kayıt döndürür. Daha fazla bilgi için bkz. [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Kayıt işlevleri](er-functions-category-record.md)
