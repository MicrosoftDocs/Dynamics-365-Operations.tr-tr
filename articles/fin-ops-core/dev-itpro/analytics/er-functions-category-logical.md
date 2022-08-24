---
title: Mantıksal kategorisindeki ER işlevlerinin listesi
description: Bu makale, Elektronik raporlama (ER) uygulamasında desteklenen mantıksal işlevler hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 02/11/2021
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
ms.openlocfilehash: 1d011968d9cfa4125e7283ca36c3558e3e79b93a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291309"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Mantıksal kategorisindeki ER işlevlerinin listesi

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) mantıksal işlevleri tek bir ifadede birden fazla karşılaştırma gerçekleştirmek veya çoklu koşulları sınamak amacıyla mantıksal değerlerle çalışmak için kullanılabilir. Bu makale, bu işlevlerin özetini sunmaktadır.

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
