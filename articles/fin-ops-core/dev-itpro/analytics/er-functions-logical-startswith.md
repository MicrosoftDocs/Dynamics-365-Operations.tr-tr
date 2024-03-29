---
title: STARTSWITH ER işlevi
description: Bu makalede, STARTSWITH Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 010646d2ab96d9a326ffb01c369726790b6377a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287233"
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
