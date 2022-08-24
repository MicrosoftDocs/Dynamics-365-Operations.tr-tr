---
title: VALUEINLARGE ER işlevi
description: Bu makalede, VALUEINLARGE Elektronik raporlama (ER) işlevinin kullanımı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 08/17/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 425dbce8f229acbb9c8d721c8f1a554989e0533c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288107"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE ER işlevi

[!include [banner](../includes/banner.md)]

`VALUEINLARGE` işlevi, *Int64* veya *Tamsayı* türündeki belirtilen girişin, belirtilen listede belirli bir öğe değeriyle eşleşip eşleşmediğini belirler. İşlev, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür. `VALUEIN` işlevinin farkını anlamak için bu makalenin ilerleyen kısımlarındaki [Kullanım notu](#usage_note) bölümüne bakın.

## <a name="syntax"></a>Sözdizimi

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Alan*

*Kayıt listesi* türünde bir veri kaynağı öğesinin geçerli yolu. Bu öğenin değeri eşleşir.

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`list item expression`: *İfade*

Geçerli koşul işaret eden ya da belirtilen listenin eşleştirmek için kullanılacak tek bir alan içeren bir ifadeyi temsil eder.

## <a name="return-values"></a>Dönüş değerleri

*Boole*

Sonuç *Boole* değeri.

## <a name=""></a><a name="usage_note">Kullanım notları</a>

Belirtilen giriş, yapılan çağrıların doğrudan SQL deyimine çevrilebildiği *Int64* veya *Integer* türündeki bir veri kaynağı öğesini temsil ettiğinde, belirtilen liste geçici bir SQL tablosuna dönüştürülür ve eşleştirme tek bir `EXISTS JOIN` sorgusu yürütülerek veritabanında gerçekleştirilir. Aksi takdirde, bu işlev [`VALUEIN`](er-functions-logical-valuein.md) işlevi olarak çalışır.

Belirtilen giriş, *Int64* ve *Tamsayı* türünden farklı bir öğe olarak tasarlanan veri kaynağı öğesini temsil ettiğinde tasarım sırasında, yapılandırılan ER ifadesi için `VALUEINLARGE` işlevinin uygulanabilir olmadığını bildiren bir hata oluşur.

`VALUEINLARGE` işlev ifadesi yürütüldüğünde ve bu yürütme kapsamında birden fazla geçici tablo kullanıldığında, çalışma zamanı hatası oluşur.

## <a name="example"></a>Örnek

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:

- *Tablo kayıtları* türünün **İçinde** veri kaynağı.
    - Bu veri kaynağı **Intrastat** tablosuna başvurur.
    - **Şirketler arası** seçeneği **Hayır** olarak ayarlanır.
- *Hesaplanan alan* türünün **InMemory** veri kaynağı.
    - Bu veri kaynağı `WHERE (In, In.Port <> "")` ifadesini içeriyor.
- *Hesaplanan alan* türünün **InFiltered** veri kaynağı.
    - Bu veri kaynağı `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)` ifadesini içeriyor.

**InFiltered** veri kaynağı, **DEMF** şirket bağlamında çağrıldıysa uygulama veritabanında yeni bir geçici tablo oluşturulur, toplanan kayıt kimliği kodları bellek içi listesi bu tabloya eklenir ve **Intrastat** tablosunun filtrelenmiş kayıtlarını döndürmek için aşağıdaki SQL deyimi oluşturulur.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)

[VALUEIN işlevleri](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
