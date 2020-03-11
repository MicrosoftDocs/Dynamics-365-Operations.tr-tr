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
ms.openlocfilehash: 2395a1932e543e35ced28a2a6e56ab44835de19a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041550"
---
# <a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER işlevi</a>

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
