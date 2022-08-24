---
title: SPLITLIST ER işlevi
description: Bu makalede, SPLITLIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 03/15/2021
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
ms.openlocfilehash: 38ac7e6c6bdf53705d1374c173422f7347253a5f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292541"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER işlevi

[!include [banner](../includes/banner.md)]

`SPLITLIST` işlev, belirtilen listeyi, her biri belirtilen sayıda kayıt içeren toplu işleri bölün. Sonra sonucu, toplu işlemlerden oluşan yeni *bir kayıt listesi* değeri olarak döndürür.

## <a name="syntax-1"></a>Sözdizimi 1

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a>Sözdizimi 2

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`number`: *Tamsayı*

Toplu iş başına maksimum kayıt sayısı

`on-demand reading flag`: *Boole*

İsteğe bağlı olarak alt liste öğelerinin oluşturulup oluşturulmayacağını belirten bir *Boole* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Aşağıdaki öğeleri içeren yeni bir toplu iş listesi olarak döndürür:

 - **Değer:** *liste*

    Geçerli toplu işe ait kayıtların listesi.

- **Batchnumber:** *tam sayı*

    Döndürülen listedeki geçerli toplu iş sayısı.

İsteğe bağlı okuma bayrağı **True** olarak ayarlandığında bellek tüketiminde azalma sağlayan, ancak öğeler sıralı olarak kullanılmıyorsa performans düşüşüne neden olabilecek alt listeler istek üzerine oluşturulur.

## <a name="example"></a>Örnek

Aşağıdaki örnekte, üç kaydın kayıt listesi olarak **Satırlar** veri kaynağı oluşturulur. Bu liste her biri en çok iki kayıt içeren toplu işlere ayrılır.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Aşağıdaki örnekte tasarlanmış biçim düzeni gösterilir. Bu biçim düzeninde, **Satırlar** veri kaynağına bağlamalar XML biçiminde çıktı üretmek için oluşturulur. Bu çıktı her toplu iş ve içindeki kayıtlar için ayrı ayrı düğümleri sunar.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
