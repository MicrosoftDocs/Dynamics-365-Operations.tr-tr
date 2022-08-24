---
title: REVERSE ER işlevi
description: Bu makalede, REVERSE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 360878319bfa29395ae5deabec2e25e52d9e0fdc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284163"
---
# <a name="reverse-er-function"></a>REVERSE ER işlevi

[!include [banner](../includes/banner.md)]

Bu `REVERSE` işlev, ters sırada sıralama düzeninde *kayıt listesi* değeri olarak belirtilen listeyi döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
REVERSE (list)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="example-1"></a>Örnek 1

*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("C|B|A", "|")` deyim içeriyorsa, `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` ifadesi **C** metin değerini döndürür.

## <a name="example-2"></a>Örnek 2

**Satıcı**, VendTable tablosuna başvuran elektronik raporlama (ER) kaynağı olarak yapılandırılırsa, `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` ifadesi, satıcıların isme göre sıralanan listesini azalan sıraya göre dizilmiş şekilde döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
