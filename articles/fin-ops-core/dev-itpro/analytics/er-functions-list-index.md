---
title: INDEX ER işlevi
description: Bu konu, INDEX Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087763"
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

> [!NOTE]
> Bu işlev için tek tabanlı numaralandırma kullanıldığından, belirtilen listenin ilk kaydını döndürmek için **1** değerini belirtin.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner (kayıt)*

Sonuç kayıt değeri.

## <a name="example-1"></a>Örnek 1

*Hesaplanmış alan* türü için veri kaynağı **DS**'yi girerseniz ve bu `SPLIT ("A|B|C", "|")` ifadesini içerirse, `DS.Value` ifadesi, bu kayıt listesinin ikinci kaydı için **B** döndürür. Bu ifade `INDEX (SPLIT ("A|B|C", "|"), 2).Value` **"B"** metin değerini de döndürür.

## <a name="example-2"></a>Örnek 2

*Hesaplanmış alan* türüne ait veri kaynağı **DS**'yi girerseniz ve `SPLIT ("A|B|C", "|")` deyim içeriyorsa, `INDEX (SPLIT ("A|B|C", "|"), 4).Value` ifadesi istisna oluşturur.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
