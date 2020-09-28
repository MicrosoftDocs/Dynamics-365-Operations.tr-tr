---
title: CN_GBT_ADDITIONALDIMENSIONID ER işlevi
description: Bu konu, CN_GBT_ADDITIONALDIMENSIONID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744443"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID ER işlevi

[!include [banner](../includes/banner.md)]

Bu `CN_GBT_ADDITIONALDIMENSIONID` işlev, belirtilen dizeden alınan tek bir mali boyut kodunu temsil eden bir *dize* değeri döndürür. Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir dize.

## <a name="syntax"></a>Sözdizimi

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir *dize* değeri.

`number`: Tamsayı

Belirtilen dizedeki istenen boyutun sıra kodunu tanımlayan *tamsayı* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)`, **"CC"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)
