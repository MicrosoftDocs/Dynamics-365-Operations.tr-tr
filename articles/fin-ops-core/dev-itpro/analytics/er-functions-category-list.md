---
title: Liste kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen liste işlevleri hakkında bilgi sağlar.
author: NickSelin
ms.date: 04/01/2020
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
ms.openlocfilehash: 4f0d9f83a1750ff51d76716147f5d16e96c0fb415608256a5dcc7524a1f2bd2f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734876"
---
# <a name="list-of-er-functions-in-the-list-category"></a>Liste kategorisindeki ER işlevlerinin listesi

[!include [banner](../includes/banner.md)]

*Kayıt listesi* ve *Konteyner (kayıt)* veri türlerinin veri kaynakları ile ilgili bilgileri ayıklamak ve üzerinde işlem gerçekleştirmek için elektronik raporlama (ER) liste işlevleri kullanılabilir. Bu konu, bu işlevlerin özetini sunmaktadır.

## <a name="list-of-supported-functions"></a>Desteklenen işlevler listesi

| İşlev | Tanım |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | Bu işlev bir bellek içi seçim olarak çalışır. Belirtilen yolla eşleşen tüm öğeleri temsil eden bir kayıt listesinden oluşan, yeni bir düzleştirilmiş *kayıt listesi* değeri döndürür. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Bu işlev birleşik bir SQL sorgusu olarak çalışır. Belirtilen yolla eşleşen tüm öğeleri temsil eden bir kayıt listesinden oluşan, yeni bir düzleştirilmiş *kayıt listesi* değeri döndürür. |
| [Say](er-functions-list-count.md)                       | Bu işlev, liste boş değilse, belirtilen listedeki kayıt sayısını gösteren bir *tamsayı* değer döndürür. Liste boşsa, bu işlev **0** (sıfır) döndürür. |
| [EmptyList](er-functions-list-emptylist.md)               | Bu işlevi, belirtilmiş olan listeyi, liste yapısı için bir kaynak olarak kullanarak boş bir *kayıt listesi* değeri döndürür.|
| [Çetele](er-functions-list-enumerate.md)               | Bu işlevi, belirtilen listenin numaralandırılmış kayıtlarından oluşan yeni bir *kayıt listesi* değeri döndürür. |
| [Filtrele](er-functions-list-filter.md)                     | Bu işlev, belirtilen koşula filtre uygulayan bir sorgu değiştirildikten sonra bir *kayıt listesi* değeri olarak belirtilmiş listeyi döndürür. |
| [İlk](er-functions-list-first.md)                       | Bu liste boş değilse, bu işlev belirtilen listenin ilk kaydını *konteyner (kayıt)* değeri olarak döndürür. Liste boşsa, bu işlev bir özel durum oluşturur. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Bu kayıt boş değilse, bu işlev belirtilen listenin ilk kaydını *konteyner (kayıt)* değeri olarak döndürür. Kayıt boş ise, bu işlev boş bir *konteyner (kayıt)* değeri döndürür. |
| [Index](er-functions-list-index.md)                       | Bu işlev, belirtilen listede belirtilen sayısal dizin kullanılarak seçilen bir *konteyner (kayıt)* değeri döndürür. Dizin listedeki kayıtların aralığı dışında ise bu işlev, bir özel durum oluşur. |
| [IsEmpty](er-functions-list-isempty.md)                   | Belirtilen listede kayıt yoksa bu işlevi bir **DOĞRU** *Boole* değeri döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür. |
| [Liste](er-functions-list-list.md)                         | Bu işlevi, belirtilen bağımsız değişkenlerden oluşturulmuş yeni listeden oluşan yeni bir *kayıt listesi* değeri döndürür.|
| [ListDistinct](er-functions-list-listdistinct.md)         | Bu işlev, belirtilen listedeki tüm kayıtlar için belirtilen ifadeyi seçici olarak hesaplar. Her benzersiz seçici değeri için tek bir kayıt içeren yeni bir *Kayıt listesi* değeri döndürür.|
| [ListJoin](er-functions-list-listjoin.md)                 | Bu işlev, belirtilen bağımsız değişkenlerden oluşturulmuş yeni birleştirilmiş listesini temsil eden yeni bir *Kayıt listesi* değeri döndürür.|
| [ListOfFields](er-functions-list-listoffields.md)         | Bu işlev,*numaralandırmanın* veya *konteyner (kayıt)* türünün belirtilen bağımsız değişkeninin yapısına göre oluşturulan bir *kayıt listesi* değeri döndürür. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Bu işlevi, belirtilen listenin yalnızca ilk kayıttan oluşan bir *kayıt listesi* değeri döndürür.|
| [OrderBy](er-functions-list-orderby.md)                   | Bu işlev belirtilen bağımsız değişkenlere göre sıralandıktan sonra belirtilen listeyi *kayıt listesi* değeri olarak döndürür. Bu bağımsız değişkenler ifadeler olarak tanımlanabilir. |
| [Ters kaydet](er-functions-list-reverse.md)                   | Bu işlev, ters sırada sıralama düzeninde *kayıt listesi* değeri olarak belirtilen listeyi döndürür. |
| [Böl](er-functions-list-split.md)                       | Bu işlev, belirtilen girdi dizesini alt dizelere böler ve sonucu yeni bir *kayıt listesi* değeri olarak döndürür. |
| [SplitList](er-functions-list-splitlist.md)               | Bu işlev, belirtilen listeyi, her biri belirtilen sayıda kayıt içeren toplu işleri bölün. Sonra sonucu, toplu işlemlerden oluşan yeni *bir kayıt listesi* değeri olarak döndürür. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Bu işlev belirtilen listeyi yeni bir alt listeler listesine (toplu işlemler) böler. Her toplu işteki kayıt sayısı dinamik olarak hesaplanır. Bu işlev, Sonra sonucu, toplu işlemlerden oluşan yeni *bir kayıt listesi* değeri olarak döndürür. |
| [StringJoin](er-functions-list-stringjoin.md)             | Bu işlevi, belirtilen listedeki belirtilen alanın art arda eklenmiş değerlerinden oluşan bir *dize* değeri döndürür. Değerler belirtilen sınırlayıcı ile ayrılır. |
| [Nerede](er-functions-list-where.md)                       | Bu işlev belirtilen koşula göre filtrelendikten sonra belirtilen listeyi *kayıt listesi* değeri olarak döndürür. |

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Elektronik raporlamada formül dili](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]