---
title: VALUEIN ER işlevi
description: Bu konu, VALUEIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: efa811df360b2ca38eb59bac849e70041405fa81
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922374"
---
# <a name="valuein-er-function"></a>VALUEIN ER işlevi

[!include [banner](../includes/banner.md)]

`VALUEIN` işlev, belirtilen girişin, belirtilen listede belirli bir öğe değerinin eşleşip eşleşmediğini belirler. Belirtilen girdi, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
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

Genel olarak, `VALUEIN` işlevi bir dizi **OR** koşuluna çevrilir. **OR** koşulları listesi büyükse ve SQL deyiminin maksimum toplam uzunluğu aşılacaksa [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) işlevini kullanabilirsiniz.

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

Bazı durumlarda, bu `EXISTS JOIN` işleci kullanılarak veritabanı SQL deyimine çevrilebilir.

> [!NOTE]
> `VALUEIN` işlevinin döndürdüğü değer, bu işlevin [`FILTER`](er-functions-list-filter.md) işlevinin mi yoksa [`WHERE`](er-functions-list-where.md) işlevinin mi seçim ölçütünü belirtmek için kullanıldığına bağlı olarak [farklı şekilde kullanılır](er-functions-list-filter.md#usage-notes).

## <a name="example-1"></a>Örnek 1

Model eşlemeniz içinde *Hesaplanan alan* türünün **Liste** veri kaynağını tanımlarsınız. Bu veri kaynağı `SPLIT ("a,b,c", ",")` ifadesini içeriyor.

Bir veri kaynağı çağrıldığında, `VALUEIN ("B", List, List.Value)` ifade olarak yapılandırıldıysa, **DOĞRU** değerini döndürür. Bu durumda, `VALUEIN` işlevi aşağıdaki bir dizi koşula çevrilir: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, `("B" = "b")` ifadesinin **DOĞRU** olduğu.

Bir veri kaynağı çağrıldığında, `VALUEIN ("B", List, LEFT(List.Value, 0))` ifade olarak yapılandırıldıysa, **YANLIŞ** değerini döndürür. Bu durumda, `VALUEIN` işlevi aşağıdaki bir dizi koşula çevrilir: `("B" = "")` ifadesinin **DOĞRU** olmadığı.

Böyle bir koşul metninde karakter sayısı üst sınırının 32.768 karakter olduğuna dikkat edin. Bu nedenle, çalışma zamanında bu sınırı aşan veri kaynakları oluşturmamanız gerekir. Sınır aşılırsa uygulama çalışmayı durdurur ve bir özel durum gönderilir. Örneğin, veri kaynağı `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` olarak yapılandırılmışsa ve **List1** ve **List2** listeleri büyük miktarda kayıt içeriyorsa bu durum ortaya çıkabilir.

Bazı durumlarda, `VALUEIN` işlevi `EXISTS JOIN` işleci kullanarak bir veritabanı ifadesi çevrilir. Bu davranış, [`FILTER`](er-functions-list-filter.md) işlevi kullanıldığında ve aşağıdaki koşullar sağlandığında gerçekleşir:

- **SORGU İSTE** seçeneği kayıtlar listesi anlamına gelen `VALUEIN` işlevinin veri kaynağı için kapatılır. Hiçbir ek koşul, çalışma zamanında bu veri kaynağına uygulanmaz.
- Kayıtlar listesi anlamına gelen `VALUEIN` işlevinin veri kaynağı için hiçbir iç içe ifade yapılandırılmaz.
- `VALUEIN` işlevinin bir liste öğesi belirtilen veri kaynağının bir alanını belirtilir (bir ifade veya bir yöntem değil).

Bu örnekte daha önce açıklanan [`WHERE`](er-functions-list-where.md) işlevi yerine bu seçeneği kullanabilirsiniz.

## <a name="example-2"></a>Örnek 2

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:

- *Tablo kayıtları* türünün **İçinde** veri kaynağı. Bu veri kaynağı Intrastat tablosuna başvurur.
- *Tablo kayıtları* türünün **Port** veri kaynağı. Bu veri kaynağı IntrastatPort tablosuna başvurur.

`FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` olarak yapılandırılmış bir veri kaynağı çağrıldığında aşağıdaki SQL ifadesi Intrastat tablosunun filtre uygulanan kayıtlarını döndürmek için oluşturulur:

```vb
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

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)

[VALUEINLARGE işlevleri](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
