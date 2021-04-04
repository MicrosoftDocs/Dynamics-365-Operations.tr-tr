---
title: Mantıksal kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen mantıksal işlevleri hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
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
ms.openlocfilehash: 7310c2b269c3f4be03102160aebe0ed164a23a5c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561674"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Mantıksal kategorisindeki ER işlevlerinin listesi

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) mantıksal işlevleri tek bir ifadede birden fazla karşılaştırma gerçekleştirmek veya çoklu koşulları sınamak amacıyla mantıksal değerlerle çalışmak için kullanılabilir. Bu konu, bu işlevlerin özetini sunmaktadır.

## <a name="list-of-supported-functions"></a>Desteklenen işlevler listesi

| İşlev | Tanım |
|----------|-------------|
| [Ve](er-functions-logical-and.md)                       | Belirtilen koşulların tümü **doğru** ise, bu işlev *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür. |
| [Sandık](er-functions-logical-case.md)                     | Bu işlev, belirtilen ifadenin değerini belirtilen alternatif seçeneklerle değerlendirir ve belirtilen ifadenin değerine eşit ilk seçeneğin sonucunu döndürür. Tersi durumda, varsayılan bir sonuç çağrılan işlevin son bağımsız değişkeni olarak bir seçenek tarafından belirtilmedikçe, isteğe bağlı bir varsayılan sonuç döndürür. Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir. |
| [İçerir](er-functions-logical-contains.md)             | Bu işlev, belirtilen girişin belirtilen metni içerip içermediğini belirler. Belirtilen giriş belirtilen metni içeriyorsa **TRUE** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür. |
| [EndsWith](er-functions-logical-endswith.md)             | Bu işlev, belirtilen girişin belirtilen metin ile bitip bitmediğini belirler. Belirtilen giriş belirtilen metinle sonlanıyorsa **TRUE** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür. |
| [Eğer](er-functions-logical-if.md)                         | Bu işlev, belirtilen koşul karşılandığında ilk belirtilen değeri döndürür. Aksi takdirde, ikinci belirtilen değeri döndürür. Döndürülen değer desteklenen veri türlerinden herhangi birinin değeri olabilir. |
| [Not](er-functions-logical-not.md)                       | Bu işlev, belirtilen koşulun ters çevrilmiş mantıksal değerini bir *Boole* değeri olarak döndürür. |
| [Veya](er-functions-logical-or.md)                         | Belirtilen koşulların tümü yanlış ise, bu işlev **yanlış** *Boole* değerini döndürür. Belirtilen koşullardan biri doğruysa bu işlev **DOĞRU** *Boole* değerini döndürür. |
| [StartsWith](er-functions-logical-startswith.md)         | Bu işlev, belirtilen girişin belirtilen metin ile başlayıp başlamadığını belirler. Belirtilen giriş belirtilen metinle başlıyorsa **TRUE** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür. |
| [ValueIn](er-functions-logical-valuein.md)               | Bu işlev, belirtilen girişin, belirtilen listede belirli bir öğe değerinin eşleşip eşleşmediğini belirler. Belirtilen girdi, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Bu işlev, *Int64* veya *Tamsayı* türündeki belirtilen girişin, belirtilen listede belirli bir öğe değeriyle eşleşip eşleşmediğini belirler. Belirtilen girdi, belirtilen listenin en az bir kaydı için belirtilen ifadenin çalıştırıldığı sonuçla eşleşirse **DOĞRU** *Boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür. |


## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Elektronik raporlamada formül dili](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]