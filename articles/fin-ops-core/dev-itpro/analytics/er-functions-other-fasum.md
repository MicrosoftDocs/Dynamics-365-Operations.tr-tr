---
title: FA_SUM ER işlevi
description: Bu konu, FA_SUM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744307"
---
# <a name="fa_sum-er-function"></a>FA_SUM ER işlevi

[!include [banner](../includes/banner.md)]

Bu `FA_SUM` işlev, belirtilen sabit kıymet maddesine, değer modeli koduna ve tarihlerin dönemine ait sabit kıymet tutarları için verilerden oluşan bir *konteyner (kayıt)* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Bağımsız değişkenler

`fixed asset code`: *Dize*

Bakiyenin hesaplandığı bir sabit kıymet maddesinin kodunu temsil eden bir *dize* değeri.

`value model code`: *Dize*

Bakiyenin hesaplandığı bir değer modeli kodunu temsil eden bir *dize* değeri.

`start date`: *Tarih*

Sabit kıymet tutarlarının hesaplandığı dönemin başlangıç tarihini temsil eden bir *tarih* değeri.

`end date`: *Tarih*

Sabit kıymet tutarlarının hesaplandığı dönemin bitiş tarihini temsil eden bir *tarih* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner (kayıt)*

Sonuç kayıt değeri.

## <a name="example"></a>Örnek

`FA_SUM ("COMP-000001", "Current", Date1, Date2)`, **geçerli** değer modeli için hazırlanan sabit kıymet **comp-000001** için **Tarih1** ile **Tarih2** arasındaki bir dönem için veri kapsayıcısını döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]