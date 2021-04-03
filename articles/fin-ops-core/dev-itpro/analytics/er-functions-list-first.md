---
title: FIRST ER işlevi
description: Bu konu, FIRST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec94a27776cf1069b50b5437f4d167019fdef120
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564747"
---
# <a name="first-er-function"></a>FIRST ER işlevi

[!include [banner](../includes/banner.md)]

Bu liste boş değilse, `FIRST` işlev belirtilen listenin ilk kaydını *konteyner (kayıt)* değeri olarak döndürür. Liste boşsa, bu işlev bir özel durum oluşturur.

## <a name="syntax"></a>Sözdizimi

```vb
FIRST (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner (kayıt)*

Sonuç kayıt değeri.

## <a name="example-1"></a>Örnek 1

Bu ifade `FIRST(SPLIT("ABC",1)).Value` **"A"** metin değerini döndürür.

## <a name="example-2"></a>Örnek 2

`FIRST(SPLIT("",1)).Value` ifadesi, çalışma zamanında bir özel durum oluşturur.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]