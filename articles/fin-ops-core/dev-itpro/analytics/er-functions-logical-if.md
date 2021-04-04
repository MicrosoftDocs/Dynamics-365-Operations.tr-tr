---
title: IF ER işlevi
description: Bu konu, IF Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565916"
---
# <a name="if-er-function"></a>IF ER işlevi

[!include [banner](../includes/banner.md)]

`IF` işlevi, belirtilen koşul karşılandığında ilk belirtilen değeri döndürür. Aksi takdirde, ikinci belirtilen değeri döndürür. Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir.

## <a name="syntax"></a>Sözdizimi

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Bağımsız değişkenler

`condition`: *Boole*

Test işlem uygulanacak geçerli bir koşullu ifade.

`first value`: *Desteklenen veri türlerinden herhangi biri*

Koşul karşılanırsa döndürülen sonuç.

`second value`: *Desteklenen veri türlerinden herhangi biri*

Koşul karşılanmazsa döndürülen sonuç.

## <a name="return-values"></a>Dönüş değerleri

*Desteklenen veri türlerinden herhangi biri*

Desteklenen veri türlerinin herhangi birinin sonuç değeri.

## <a name="usage-notes"></a>Kullanım notları

`first value` ve `second value` bağımsız değişkenlerin aynı veri türü kullanılarak belirtilmesi gerekir. Yapılandırılan değerlerin veri türleri eşleşmezse, tasarım zamanında özel durum oluşturulur.

İlk değer ve ikinci değer *konteyner (kayıt)* veya *kayıt listesi* veri türünün değerleri ise, sonuç yalnızca her iki değerde bulunan alanlara sahiptir.

## <a name="example"></a>Örnek

`IF (1=2, "condition is met", "condition is not met")`, **Koşul karşılanmadığında** dizesini döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]