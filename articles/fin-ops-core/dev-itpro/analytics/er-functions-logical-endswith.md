---
title: ENDSWITH ER işlevi
description: Bu makalede, ENDSWITH Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 8b054a255cb3ba945a7825a0032e54f5ac3ad127
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855688"
---
# <a name="endswith-er-function"></a>ENDSWITH ER işlevi

[!include [banner](../includes/banner.md)]

`ENDSWITH` işlevi, belirtilen girişin belirtilen metin ile bitip bitmediğini belirler. Belirtilen giriş belirtilen metinle sonlanıyorsa **TRUE** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Dize*

Değeri, ikinci bağımsız değişkenle bitebilecek *Dize* türünün veya dize sabitinin bir veri kaynağı öğesinin geçerli yolu.

`start text`: *Dize*

Değeri, ilk bağımsız değişkenin sonunda olabilecek *Dize* veri türünün veya dize sabitinin bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Boole*

Sonuç *Boole* değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlev, yalnızca ilgili eşleme, [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)'de [Microsoft Dataverse](/power-platform/admin/data-integrator) öğesine erişmek için yapılandırıldığında [FILTER](er-functions-list-filter.md) işlevinin bir koşul ifadesini belirlemek için kullanılabilir. Aksi durumda, tasarım zamanında özel durum oluşturulur. Aldığınız iletide, verimliliği artırmaya yardımcı olmak için `FILTER` işlevi yerine [WHERE](er-functions-list-where.md) işlevini kullanmanız önerilir.

## <a name="example-1"></a>Örnek 1

`ENDSWITH ("abc", "d")` ifadesi **yanlış** değerini, `ENDSWITH ("abc", "C")` ise **doğru** değerini döndürür.

## <a name="example-2"></a>Örnek 2

**Model** veri kaynağının **adres** alanı değeri **USA** dizesiyle sona eriyorsa `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` ifadesi **doğru**'yu döndürür. Aksi takdirde **YANLIŞ**'ı döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)
