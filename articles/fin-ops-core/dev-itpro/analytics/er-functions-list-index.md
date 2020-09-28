---
title: INDEX ER işlevi
description: Bu konu, INDEX Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745196"
---
# <a name="index-er-function"></a>INDEX ER işlevi

[!include [banner](../includes/banner.md)]

Bu `INDEX` işlev, belirtilen listede belirtilen sayısal dizin kullanılarak seçilen bir *konteyner (kayıt)* değeri döndürür. Dizin listedeki kayıtların aralığı dışında ise bir özel durum oluşur.

## <a name="syntax"></a>Sözdizimi

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`index`: *Tamsayı*

İstenen kaydın belirtilen listedeki konumunu gösteren sayısal dizin.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner (kayıt)*

Sonuç kayıt değeri.

## <a name="example-1"></a>Örnek 1

*Hesaplanmış alan* türü için veri kaynağı **DS**'yi girerseniz ve bu `SPLIT ("A|B|C", "|")` ifadesini içerirse, `DS.Value` ifadesi, bu kayıt listesinin ikinci kaydı için **B** döndürür. Bu ifade `INDEX (SPLIT ("A|B|C", "|"), 2).Value` **"B"** metin değerini de döndürür.

## <a name="example-2"></a>Örnek 2

*Hesaplanmış alan* türüne ait veri kaynağı **DS**'yi girerseniz ve `SPLIT ("A|B|C", "|")` deyim içeriyorsa, `INDEX (SPLIT ("A|B|C", "|"), 4).Value` ifadesi istisna oluşturur.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)
