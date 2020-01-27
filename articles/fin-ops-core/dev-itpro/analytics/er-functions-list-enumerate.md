---
title: ENUMERATE ER işlevi
description: Bu konu, ENUMERATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: f0a1c83ee869810e816b6d32ea890d172d2910e5
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916235"
---
# <a name="ENUMERATE">ENUMERATE ER işlevi</a>

[!include [banner](../includes/banner.md)]

Bu `ENUMERATE` işlevi, belirtilen listenin numaralandırılmış kayıtlarından oluşan yeni bir *kayıt listesi* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```
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
