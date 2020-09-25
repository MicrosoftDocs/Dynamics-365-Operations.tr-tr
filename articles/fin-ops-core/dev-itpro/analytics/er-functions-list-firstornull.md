---
title: FIRSTORNULL ER işlevi
description: Bu konu, FIRSTORNULL Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: e360812c5b0dbfb8df4ab279bf3e0050acebbb25
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745212"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL ER işlevi

[!include [banner](../includes/banner.md)]

Bu kayıt boş değilse, `FIRSTORNULL` işlev belirtilen listenin ilk kaydını *konteyner (kayıt)* değeri olarak döndürür. Kayıt boş ise, bu işlev boş bir *konteyner (kayıt)* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner (kayıt)*

Sonuç kayıt değeri.

## <a name="example"></a>Örnek

İfade `FIRSTORNULL(SPLIT("",1)).Value` boş bir dize (**""**) döndürüyor.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)
