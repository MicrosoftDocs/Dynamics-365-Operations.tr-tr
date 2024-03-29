---
title: CASE ER işlevi
description: Bu makalede, CASE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 702648e14abe980d246b92b0fe512bba07717e45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274874"
---
# <a name="case-er-function"></a>CASE ER işlevi

[!include [banner](../includes/banner.md)]

`CASE` işlev, belirtilen ifadenin değerini belirtilen alternatif seçeneklerle değerlendirir ve belirtilen ifadenin değerine eşit ilk seçeneğin sonucunu döndürür. Tersi durumda, varsayılan bir sonuç çağrılan işlevin son bağımsız değişkeni olarak bir seçenek tarafından belirtilmedikçe, isteğe bağlı bir varsayılan sonuç döndürür. Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir.

## <a name="syntax"></a>Sözdizimi

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Bağımsız değişkenler

`expression`: *Temel veri türü* (Boole, sayısal veya metin)

Temel veri türü değerini döndüren geçerli bir ifade.

`option 1`: *Temel veri türü* (Boole, sayısal veya metin)

Çağrılan işlevin `expression` bağımsız değişkeniyle aynı temel veri türü değerini döndüren geçerli bir ifade. Bu bağımsız değişken gereklidir.

`result 1`: *Desteklenen veri türlerinden herhangi biri*

Önceki seçeneğe karşılık gelen iade sonucu. Bu bağımsız değişken gereklidir.

`option N`: *Temel veri türü* (Boole, sayısal veya metin)

Çağrılan işlevin `expression` bağımsız değişkeniyle aynı temel veri türü değerini döndüren geçerli bir ifade. Bu bağımsız değişken isteğe bağlıdır.

`result N`: *Desteklenen veri türlerinden herhangi biri*

Önceki seçeneğe karşılık gelen iade sonucu. Bu bağımsız değişken isteğe bağlıdır.

`default result`: *Desteklenen veri türlerinden herhangi biri*

Eşleşme yoksa, döndürülmesi gereken sonuç. Bu bağımsız değişken isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Desteklenen veri türlerinden herhangi biri*

Desteklenen veri türlerinin herhangi birinin sonuç değeri.

## <a name="usage-notes"></a>Kullanım notları

Çalışma zamanında bir eşleşme yoksa ve isteğe bağlı olarak bir varsayılan sonuç tanımlanmamışsa, bir özel durum atılır.

Tüm sonuçların aynı veri türü kullanılarak belirtilmesi gerekir. Yapılandırılan sonuçların veri türleri eşleşmezse, tasarım zamanında özel durum oluşturulur.

İlk sonuç değeri ve *N*'ci sonuç değer *konteyner (kayıt)* veya *kayıt listesi* veri türünün değerleri ise, sonuç yalnızca her iki değerde bulunan alanlara sahiptir.

## <a name="example"></a>Örnek

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")`, geçerli uygulama oturum tarihi, Ekim ve Aralık arasında ise, **"kış"** dizesini döndürür. Aksi halde, boş bir dize döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
