---
title: CONTAINS ER işlevi
description: Bu konu, CONTAINS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 81964681688cebf870bc9b6c59aff0b7fdd82449
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557560"
---
# <a name="contains-er-function"></a>CONTAINS ER işlevi

[!include [banner](../includes/banner.md)]

`CONTAINS` işlevi, belirtilen girişin belirtilen metni içerip içermediğini belirler. Belirtilen giriş belirtilen metni içeriyorsa **TRUE** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Dize*

Değeri, ikinci bağımsız değişkeni içerebilecek *Dize* türünün veya dize sabitinin bir veri kaynağı öğesinin geçerli yolu.

`search text`: *Dize*

Değeri, ilk bağımsız değişkende bulunabilecek *Dize* veri türünün veya dize sabitinin bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Boole*

Sonuç *Boole* değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlev, yalnızca ilgili eşleme, [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)'de [Microsoft Dataverse](../data-entities/data-integration-cds.md) öğesine erişmek için yapılandırıldığında [FILTER](er-functions-list-filter.md) işlevinin bir koşul ifadesini belirlemek için kullanılabilir. Aksi durumda, tasarım zamanında özel durum oluşturulur. Aldığınız iletide, verimliliği artırmaya yardımcı olmak için `FILTER` işlevi yerine [WHERE](er-functions-list-where.md) işlevini kullanmanız önerilir.

## <a name="example-1"></a>Örnek 1

`CONTAINS ("abc", "d")` ifadesi **yanlış** değerini, `CONTAINS ("abc", "C")` ise **doğru** değerini döndürür.

## <a name="example-2"></a>Örnek 2

**Model** veri kaynağının **adres** alanı değeri **DEU** dizesini içeriyorsa `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` ifadesi **TRUE**'yu döndürür. Aksi takdirde **YANLIŞ**'ı döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)