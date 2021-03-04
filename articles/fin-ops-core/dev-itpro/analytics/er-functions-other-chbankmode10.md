---
title: CH_BANK_MOD_10 ER işlevi
description: Bu konu, CH_BANK_MOD_10 Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bca82cd596ba1e3ec42b3dba91ee6c4871ff8601
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686870"
---
# <a name="ch_bank_mod_10-er-function"></a>CH_BANK_MOD_10 ER işlevi

[!include [banner](../includes/banner.md)]

Bu `CH_BANK_MOD_10` işlev, bir alacaklı başvurusunu, belirtilen fatura numarasının basamaklara dayalı olarak MOD10 ifadesi olarak gösteren bir *dize* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Bağımsız değişkenler

`invoice number digits`: *Dize*

Fatura numarasının rakamlarını temsil eden metin değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`CH_BANK_MOD_10 ("VEND-200002")`, **3** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]