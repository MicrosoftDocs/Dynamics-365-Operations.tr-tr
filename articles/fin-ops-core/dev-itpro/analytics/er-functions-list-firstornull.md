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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3547eeea3c6fef5cca0699002cc0c35cffd940b3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688055"
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
