---
title: ORDERBY ER işlevi
description: Bu konu, ORDERBY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c39700fab90265ed1915b4815a6bb27af58d9516
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686476"
---
# <a name="orderby-er-function"></a>ORDERBY ER işlevi

[!include [banner](../includes/banner.md)]

`ORDERBY` işlev belirtilen bağımsız değişkenlere göre sıralandıktan sonra belirtilen listeyi *kayıt listesi* değeri olarak döndürür. Bu bağımsız değişkenler ifadeler olarak tanımlanabilir.

## <a name="syntax"></a>Sözdizimi

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`expression 1`: *Alan*

Çağrılan işlevin `list` bağımsız değişkeni tarafından başvurulan bir veri kaynağı alanının geçerli yolu. Referans gösterilen alan, ilkel veri türünde bir alan olmalıdır. Bu bağımsız değişken gereklidir.

`expression N`: *Alan*

Çağrılan işlevin `list` bağımsız değişkeni tarafından başvurulan bir veri kaynağı alanının geçerli yolu. Referans gösterilen alan, ilkel veri türünde bir alan olmalıdır. Bu ek bağımsız değişkenler isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="example-1"></a>Örnek 1

*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("C|B|A", "|")` deyim içeriyorsa, `FIRST( ORDERBY( DS, DS. Value)).Value` ifadesi **A** metin değerini döndürür.

## <a name="example-2"></a>Örnek 2

**Satıcı**, VendTable tablosuna başvuran elektronik raporlama (ER) kaynağı olarak yapılandırılırsa, `ORDERBY (Vendors, Vendors.'name()')` ifadesi, satıcıların isme göre sıralanan listesini artan sıraya göre dizilmiş şekilde döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]