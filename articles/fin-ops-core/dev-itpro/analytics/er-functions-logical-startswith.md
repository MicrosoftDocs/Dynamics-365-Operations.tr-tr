---
title: STARTSWITH ER işlevi
description: Bu konu, STARTSWITH Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: b378f501ccf812cfa0ae09e7cfbfdcf4c8a24ab8747b8ffe6044769df14a3057
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762236"
---
# <a name="startswith-er-function"></a>STARTSWITH ER işlevi

[!include [banner](../includes/banner.md)]

`STARTSWITH` işlevi, belirtilen girişin belirtilen metin ile başlayıp başlamadığını belirler. Belirtilen giriş belirtilen metinle başlıyorsa **TRUE** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Dize*

Değeri, ikinci bağımsız değişkenle başlayabilecek *Dize* türünün veya dize sabitinin bir veri kaynağı öğesinin geçerli yolu.

`start text`: *Dize*

Değeri, ilk bağımsız değişkenin başında olabilecek *Dize* veri türünün veya dize sabitinin bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Boole*

Sonuç *Boole* değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlev, yalnızca ilgili eşleme, [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md)'de [Microsoft Dataverse](/power-platform/admin/data-integrator) öğesine erişmek için yapılandırıldığında [FILTER](er-functions-list-filter.md) işlevinin bir koşul ifadesini belirlemek için kullanılabilir. Aksi durumda, tasarım zamanında özel durum oluşturulur. Aldığınız iletide, verimliliği artırmaya yardımcı olmak için `FILTER` işlevi yerine [WHERE](er-functions-list-where.md) işlevini kullanmanız önerilir.

## <a name="example-1"></a>Örnek 1

`STARTSWITH ("abc", "d")` ifadesi **yanlış** değerini, `STARTSWITH ("abc", "A")` ise **doğru** değerini döndürür.

## <a name="example-2"></a>Örnek 2

**Model** veri kaynağının **adres** alanı değeri **123 Coffee Street** dizesiyle başlıyorsa `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` ifadesi **doğru**'yu döndürür. Aksi takdirde **YANLIŞ**'ı döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)
