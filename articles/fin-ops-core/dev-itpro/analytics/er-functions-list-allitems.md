---
title: ALLITEMS ER işlevi
description: Bu makalede, ALLITEMS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: bb469955c66baf875eea80dde8199986e69e2e71
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274124"
---
# <a name="allitems-er-function"></a>ALLITEMS ER işlevi

[!include [banner](../includes/banner.md)]

`ALLITEMS` işlevi, bellek içi seçim olarak çalışır ve belirtilen yolla eşleşen tüm öğeleri temsil eden kayıtların listesi olarak yeni bir düzleştirilmiş *kayıt listesi* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Bağımsız değişkenler

`path`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Yol, *kayıt listesi* veri türünün veri kaynağı öğesine geçerli veri kaynağı yolu olarak tanımlanmalıdır. Dize yolu ve tarih gibi veri öğeleri, elektronik raporlama (ER) ifade oluşturucuda tasarım zamanında hata vermelidir.

Büyük miktarda veri içerebilen işlem veri kaynakları için bu işlevi kullanmanızı önermeyiz. Bunun yerine, [ALLTEMSQUERY](er-functions-list-allitemsquery.md) işlevini kullanmayı düşünebilirsiniz.

## <a name="example-1"></a>Örnek 1

`SPLIT("abcdef" , 2)` veri kaynağı **DS** olarak girerseniz, ifade `COUNT( ALLITEMS (DS))` **3** döndürür.

## <a name="example-2"></a>Örnek 2

VendTable uygulama tablosuna başvuran *kayıt listesi* veri türünün veri kaynağına **Vend** değerini girerseniz `ALLITEMS (Vend.'<Relations'.ContactPerson)` ifadesi, **ContactPerson** yapısına sahip bir kayıt listesi döndürür ve **ContactPerson.ContactForParty == VendTable.Party** ilişkisi kullanılarak erişilebilen tüm irtibat kişilerini içerir.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
