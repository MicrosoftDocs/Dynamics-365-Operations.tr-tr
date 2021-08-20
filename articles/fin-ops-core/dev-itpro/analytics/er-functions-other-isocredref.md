---
title: ISOCREDREF ER işlevi
description: Bu konu, ISOCREDREF Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/17/2019
ms.prod: ''
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
ms.openlocfilehash: e13b9bacc642917e6a520968630fc75fb30bc9dc3fd02b2d9aa3cfb2ceb33790
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737939"
---
# <a name="isocredref-er-function"></a>ISOCREDREF ER işlevi

[!include [banner](../includes/banner.md)]

`ISOCREDREF` işlevi, bir Uluslararası Standartlar Kuruluşu (ISO) alacaklı başvurusunu, belirtilen fatura numarasının basamakları ve alfabetik sembollerine dayalı olarak temsil eden *Dize* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Bağımsız değişkenler

`invoice number digits`: *Dize*

Fatura numarasının rakamlarını temsil eden metin değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

> [!NOTE] 
> ISO uyumlu olmayan alfabelerden sembolleri elemek için, `invoice number digits` bağımsız değişkeni işleve gönderilmeden önce çevrilmesi gerekir.

## <a name="example"></a>Örnek

`ISOCredRef ("VEND-200002")`, **"RF23VEND-200002"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]