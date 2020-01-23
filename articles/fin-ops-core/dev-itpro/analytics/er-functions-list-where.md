---
title: WHERE ER işlevi
description: Bu konu, WHERE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 50d90697f522f3c4d7b62190928008b6d923ffc6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916097"
---
# <a name="WHERE">WHERE ER işlevi</a>

[!include [banner](../includes/banner.md)]

`WHERE` işlev belirtilen koşula göre filtrelendikten sonra belirtilen listeyi *kayıt listesi* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```
WHERE (list, condition)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`condition`: *Boole*

Belirtilen listenin kayıtlarını filtrelemek için kullanılan geçerli bir koşullu ifade.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

[FILTER](er-functions-list-filter.md) işlevinden farklı olarak bu işlev, belirtilen koşul bellekteki *Kayıt listesi* türünün herhangi bir Elektronik raporlama (ER) veri kaynağına uygulanabilir.

Bu işlev için yapılandırılmış olan bağımsız değişkenler (`list` ve `condition`) bu isteğin doğrudan SQL aramasına çevrilmesine izin veriyorsa, tasarım zamanında bir uyarı mesajı oluşturulur. Bu ileti kullanıcıya `WHERE` yerine [FILTER](er-functions-list-filter.md) işlevi kullanılıyorsa performansın iyileşme olasılığı olduğunu bildirir.

## <a name="example-1"></a>Örnek 1

**Satıcı**, VendTable tablosuna başvuran ER kaynağı olarak yapılandırılırsa, `WHERE (Vendors, Vendors.VendGroup = "40")` ifadesi, yalnızca grup 40'a dahil olan satıcıların listesini döndürür.

## <a name="example-2"></a>Örnek 2

*Hesaplanmış alan* türü için veri kaynağı **DS**'yi girerseniz ve bu `SPLIT ("A|B|C", "|")` ifadesini içerirse, `WHERE( DS, DS.Value = "B")` ifadesi, **Değer** alanında **"B"** metni içeren tek bir kayıt listesi döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)