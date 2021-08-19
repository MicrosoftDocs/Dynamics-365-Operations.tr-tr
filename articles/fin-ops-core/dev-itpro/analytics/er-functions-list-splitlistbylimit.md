---
title: SPLITLISTBYLIMIT ER işlevi
description: Bu konu, SPLITLISTBYLIMIT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 52351c131480119ce9fb98a75307ebf6026cb12b9977e8b4236d3a24ef6a140e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744446"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT ER işlevi

[!include [banner](../includes/banner.md)]

`SPLITLISTBYLIMIT` işlev belirtilen listeyi yeni bir alt listeler listesine (toplu işlemler) böler. Her toplu işteki kayıt sayısı dinamik olarak hesaplanır. Bu işlev, Sonra sonucu, toplu işlemlerden oluşan yeni *bir kayıt listesi* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`limit value`: *Tamsayı* veya *Gerçek*

Orijinal listeyi toplu işlemlere Bölmek için kullanılan maksimum sınır değeri.

`limit source`: *Alan*

*Tamsayı* veya *Gerçek* veri alanının geçerli yolu belirtilen listeyi yazın. Bu alanın değeri, toplam toplamın artmakta olduğu adımı tanımlar.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Aşağıdaki öğeleri içeren yeni bir toplu iş listesi olarak döndürür:

- **Değer**: *liste*

    Geçerli toplu işe ait kayıtların listesi.

- **Batchnumber**: *tam sayı*

    Döndürülen listedeki geçerli toplu iş sayısı.

Sınır kaynağı tanımlanan sınırı aştığında sınır, kaynak listedeki tek bir öğeye uygulanmaz.

## <a name="example"></a>Örnek

Aşağıdaki şekil, elektronik raporlama (ER) biçimi gösterir.

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Aşağıdaki şekilde, biçim için kullanılan veri kaynakları gösterilmektedir.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Aşağıdaki örnekte biçim çalıştırıldığında elde edilen sonuç gösterilir. Bu durumda, çıktı emtia maddelerinin düz listesi olur.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

Aşağıdaki örneklerde, tek bir toplu iş 9 limitini geçmemesi gereken toplam ağırlığa sahip emtiaları içerdiğinde, emtia maddelerinin listesini toplu işlerde ayarlananla aynı biçimde gösterir.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Aşağıdaki örnekte düzeltilen biçim çalıştırıldığında elde edilen sonuç gösterilir.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Sınırının kaynak (**ağırlık**) değeri (**11**) tanımlanan sınırı (**9**) geçtiğinden sınır, kaynak listedeki son maddeye uygulanmaz. Rapor oluşturma sırasında alt listeleri yok saymak için, gerekirse `WHERE` işlevini veya ilgili biçim öğesinin **Etkinleştirildi** ifadesini kullanın.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]