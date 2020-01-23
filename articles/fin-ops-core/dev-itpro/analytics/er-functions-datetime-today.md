---
title: TODAY ER işlevi
description: Bu konu, TODAY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c7e9917dcdc45a52e0ad490f5fa194d5390cc437
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917431"
---
# <a name="TODAY">TODAY ER işlevi</a>

[!include [banner](../includes/banner.md)]

`TODAY` işlev, geçerli uygulama sunucusu tarih temsil eden bir *Tarih* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```
TODAY ()
```

## <a name="return-values"></a>Dönüş değerleri

*Tarih*

Sonuç tarih değeri.

## <a name="example"></a>Örnek

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarihini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)
