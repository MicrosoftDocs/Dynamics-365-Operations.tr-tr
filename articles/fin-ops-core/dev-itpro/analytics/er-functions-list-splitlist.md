---
title: SPLITLIST ER işlevi
description: Bu konu, SPLITLIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 950fc711f0e28eaee7fabc437ee16a022e1b705e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744803"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER işlevi

[!include [banner](../includes/banner.md)]

`SPLITLIST` işlev, belirtilen listeyi, her biri belirtilen sayıda kayıt içeren toplu işleri bölün. Sonra sonucu, toplu işlemlerden oluşan yeni *bir kayıt listesi* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`number`: *Tamsayı*

Toplu iş başına maksimum kayıt sayısı

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Aşağıdaki öğeleri içeren yeni bir toplu iş listesi olarak döndürür:

 - **Değer:** *liste*

    Geçerli toplu işe ait kayıtların listesi.

- **Batchnumber:** *tam sayı*

    Döndürülen listedeki geçerli toplu iş sayısı.

## <a name="example"></a>Örnek

Aşağıdaki örnekte, üç kaydın kayıt listesi olarak **Satırlar** veri kaynağı oluşturulur. Bu liste her biri en çok iki kayıt içeren toplu işlere ayrılır.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Aşağıdaki örnekte tasarlanmış biçim düzeni gösterilir. Bu biçim düzeninde, **Satırlar** veri kaynağına bağlamalar XML biçiminde çıktı üretmek için oluşturulur. Bu çıktı her toplu iş ve içindeki kayıtlar için ayrı ayrı düğümleri sunar.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)
