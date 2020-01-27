---
title: LISTOFFIRSTITEM ER işlevi
description: Bu konu, LISTOFFIRSTITEM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 4d985ef5015bc104a83260b64418821cc715e8cb
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917270"
---
# <a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER işlevi</a>

[!include [banner](../includes/banner.md)]

Bu `LISTOFFIRSTITEM` işlevi, belirtilen listenin yalnızca ilk kayıttan oluşan bir *kayıt listesi* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="example"></a>Örnek

Bu ifade `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` **"A"** metin değerini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)
