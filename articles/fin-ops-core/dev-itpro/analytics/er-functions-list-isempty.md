---
title: ISEMPTY ER işlevi
description: Bu konu, ISEMPTY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: c8450c17fe2de964016951197b0d4e231c550a99
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916143"
---
# <a name="ISEMPTY">ISEMPTY ER işlevi</a>

[!include [banner](../includes/banner.md)]

Belirtilen listede kayıt yoksa `ISEMPTY` işlevi bir **DOĞRU** *Boolean* değeri döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```
ISEMPTY (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Boole*

Sonuç *Boole* değeri.

## <a name="example-1"></a>Örnek 1

*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("A|B|C", "|")` deyim içeriyorsa, `ISEMPTY(DS)` ifadesi **yanlış** döndürür.

## <a name="example-2"></a>Örnek 2

`ISEMPTY (SPLIT ("",1))` ifadesi **DOĞRU** değerini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)