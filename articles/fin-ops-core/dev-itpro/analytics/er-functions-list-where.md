---
title: WHERE ER işlevi
description: Bu konu, WHERE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: bdf5c658fda83399c7bcffeaaf07005164c53f8a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745509"
---
# <a name="where-er-function"></a>WHERE ER işlevi

[!include [banner](../includes/banner.md)]

`WHERE` işlev belirtilen koşula göre filtrelendikten sonra belirtilen listeyi *kayıt listesi* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]