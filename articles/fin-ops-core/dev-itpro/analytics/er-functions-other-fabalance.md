---
title: FA_BALANCE ER işlevi
description: Bu makalede, FA_BALANCE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: c3dd44f0d5ff143189b2c55c4df80847c2161231
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902697"
---
# <a name="fa_balance-er-function"></a>FA_BALANCE ER işlevi

[!include [banner](../includes/banner.md)]

`FA_BALANCE` işlev, belirtilen sabit kıymet maddesine, değer modeli koduna, raporlama yılına ve raporlama tarihlerin dönemine ait sabit kıymet bakiyesi için verilerden oluşan bir *konteyner (kayıt)* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Bağımsız değişkenler

`fixed asset code`: *Dize*

Bakiyenin hesaplandığı bir sabit kıymet maddesinin kodunu temsil eden bir *dize* değeri.

`value model code`: *Dize*

Bakiyenin hesaplandığı bir değer modeli kodunu temsil eden bir *dize* değeri.

`reporting year`: *Numaralandırma değeri*

Bakiye hesaplaması için bir dönem tanımlayan **VarlıkYılı** uygulama numaralandırmasının sabit listesi değeri.

`reporting date`: *Tarih*

Bakiye hesaplaması için bir tarih tanımlayan *tarih* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner (kayıt)*

Sonuç kayıt değeri.

## <a name="example"></a>Örnek

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())`, geçerli uygulama oturum tarihinde **Geçerli** değer modeline sahip **COMP-000001** sabit kıymet bakiyeleri için hazırlanan veri kapsayıcısını döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]