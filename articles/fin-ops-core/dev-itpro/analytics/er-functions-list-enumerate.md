---
title: ENUMERATE ER işlevi
description: Bu konu, ENUMERATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
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
ms.openlocfilehash: b05448b57d3b08af61144dacdfa2a4e1ba30d009
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746663"
---
# <a name="enumerate-er-function"></a>ENUMERATE ER işlevi

[!include [banner](../includes/banner.md)]

Bu `ENUMERATE` işlevi, belirtilen listenin numaralandırılmış kayıtlarından oluşan yeni bir *kayıt listesi* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ENUMERATE (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Döndürülen numaralandırılmış kayıtların listesi aşağıdaki ek öğeleri sunar:

- Alanlar kaydı (**Değer** bileşeni)
- Geçerli kayıt dizini (**Numara** bileşeni)

## <a name="example"></a>Örnek

Aşağıdaki örnekte, **Numaralandırılan** veri kaynağı, VendTable tablosuna başvuran **Satıcılar** veri kaynağındaki satıcı kayıtlarının numaralandırılmış bir listesi olarak oluşturulur.

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

Aşağıdaki şekil, elektronik raporlama (ER) biçimi gösterir. Bu biçimde, veri bağlamaları XML biçiminde çıktı üretmek için oluşturulur. Bu çıktı ayrı ayrı satıcıları numaralandırılmış düğümler olarak gösterir.

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]