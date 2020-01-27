---
title: VALUEIN ER işlevi
description: Bu konu, VALUEIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915982"
---
# <a name="VALUEIN">VALUEIN ER işlevi</a>

[!include [banner](../includes/banner.md)]

`VALUEIN` işlev, belirtilen girişin, belirtilen listede belirli bir öğe değerinin eşleşip eşleşmediğini belirler. Belirtilen girdi, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Alan*

*Kayıt listesi* türünde bir veri kaynağı öğesinin geçerli yolu. Bu öğenin değeri eşleşir.

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`list item expression`: *Boole*

Geçerli koşul işaret eden ya da belirtilen listenin eşleştirmek için kullanılacak tek bir alan içeren bir ifadeyi temsil eder.

## <a name="return-values"></a>Dönüş değerleri

*Boole*

Sonuç *Boole* değeri.

## <a name="usage-notes"></a>Kullanım notları

Genel olarak, `VALUEIN` işlevi bir dizi **OR** koşuluna çevrilir.

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

Bazı durumlarda, bu `EXISTS JOIN` işleci kullanılarak veritabanı SQL deyimine çevrilebilir.

## <a name="example-1"></a>Örnek 1

Model eşlemeniz içinde *Hesaplanan alan* türünün **Liste** veri kaynağını tanımlarsınız. Bu veri kaynağı `SPLIT ("a,b,c", ",")` ifadesini içeriyor.

Bir veri kaynağı çağrıldığında, `VALUEIN ("B", List, List.Value)` ifade olarak yapılandırıldıysa, **DOĞRU** değerini döndürür. Bu durumda, `VALUEIN` işlevi aşağıdaki bir dizi koşula çevrilir: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, `("B" = "b")` ifadesinin **DOĞRU** olduğu.

Bir veri kaynağı çağrıldığında, `VALUEIN ("B", List, LEFT(List.Value, 0))` ifade olarak yapılandırıldıysa, **YANLIŞ** değerini döndürür. Bu durumda, `VALUEIN` işlevi aşağıdaki bir dizi koşula çevrilir: `("B" = "")` ifadesinin **DOĞRU** olmadığı.

Böyle bir koşul metninde karakter sayısı üst sınırının 32.768 karakter olduğuna dikkat edin. Bu nedenle, çalışma zamanında bu sınırı aşan veri kaynakları oluşturmamanız gerekir. Sınır aşılırsa uygulama çalışmayı durdurur ve bir özel durum gönderilir. Örneğin, veri kaynağı `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` olarak yapılandırılmışsa ve **List1** ve **List2** listeleri büyük miktarda kayıt içeriyorsa bu durum ortaya çıkabilir.

Bazı durumlarda, `VALUEIN` işlevi `EXISTS JOIN` işleci kullanarak bir veritabanı ifadesi çevrilir. Bu davranış, [FİLTRE](er-functions-list-filter.md) işlevi kullanıldığında ve aşağıdaki koşullar sağlandığında olur:

- **SORGU İSTE** seçeneği kayıtlar listesi anlamına gelen `VALUEIN` işlevinin veri kaynağı için kapatılır. Hiçbir ek koşul, çalışma zamanında bu veri kaynağına uygulanmaz.
- Kayıtlar listesi anlamına gelen `VALUEIN` işlevinin veri kaynağı için hiçbir iç içe ifade yapılandırılmaz.
- `VALUEIN` işlevinin bir liste öğesi belirtilen veri kaynağının bir alanını belirtilir (bir ifade veya bir yöntem değil).

Bu örnekte daha önce açıklandığı gibi [WHERE](er-functions-list-where.md) işlevi yerine bu seçeneği kullanmayı düşünün.

## <a name="example-2"></a>Örnek 2

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:

- *Tablo kayıtları* türünün **İçinde** veri kaynağı. Bu veri kaynağı Intrastat tablosuna başvurur.
- *Tablo kayıtları* türünün **Port** veri kaynağı. Bu veri kaynağı IntrastatPort tablosuna başvurur.

`FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` olarak yapılandırılmış bir veri kaynağı çağrıldığında aşağıdaki SQL ifadesi Intrastat tablosunun filtre uygulanan kayıtlarını döndürmek için oluşturulur:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

**dataAreaId** alanları için nihai SQL deyimi `IN` işleci kullanılarak oluşturulur.

## <a name="example-3"></a>Örnek 3

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:

- **Le** veri kaynağına *hesaplanan alan* ekleyin. Bu veri kaynağı `SPLIT ("DEMF,GBSI,USMF", ",")` ifadesini içeriyor.
- *Tablo kayıtları* türünün **İçinde** veri kaynağı. Bu veri kaynağı Intrastat tablosuna başvuruyor ve bunun için **şirketler arası** seçeneği açık.

`FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` ifadesi olarak yapılandırılmış bir veri kaynağı çağrıldığında son SQL deyimi aşağıdaki koşulu içerir.

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)
