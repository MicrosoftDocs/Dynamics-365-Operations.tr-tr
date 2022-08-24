---
title: WEEKNUM ER işlevi
description: Bu makalede, WEEKNUM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268161"
---
# <a name="weeknum-er-function"></a>WEEKNUM ER işlevi

[!include [banner](../includes/banner.md)]

`WEEKNUM` işlevi, belirtilen *[Tarih](er-formula-supported-data-types-primitive.md#date)* değerini içeren yılın haftasını temsil eden bir *[Tamsayı](er-formula-supported-data-types-primitive.md#integer)* değeri döndürür. Hesaplama, takvim haftasını ve haftanın ilk gününü tanımlayan kültüre bağımlı kuralları temel alandır.

## <a name="syntax"></a>Sözdizimi

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Bağımsız değişkenler</a>

`date`: *Tarih*

Yılın haftasını hesaplamak için kullanılacak tarihi temsil eden tarih değeri.

`culture`: *[Dize](er-formula-supported-data-types-primitive.md#string)*

Hesaplama için kullanılacak kültür. .NET [standartlarına](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0) uygun olarak desteklenen kültür kodlarını kullanabilirsiniz.

## <a name="return-values"></a>Dönüş değerleri

*Tamsayı*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu standart, yerel bölgenin çalışma zamanında sağlandığı bir ülke veya bölge tarafından kabul edilmişse yılın haftası [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) standardına göre hesaplanır. Aksi takdirde, hesaplama ülkeye/bölgeye özgü ulusal standartlara dayanır.

Desteklenmeyen bir [kültür](#arguments) kodu çalışma zamanında `WEEKNUM` işlevinin bağımsız değişkeni olarak sağlanırsa bir özel durum oluşturulur. Boş dize kültür kodu olarak sağlanmışsa hafta numarasını hesaplamak için İngilizce ülkeden bağımsız takvim kullanılır.

## <a name="examples"></a>Örnekler

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))`, **1** döndürür.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))`, **53** döndürür.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))`, **52** döndürür.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))`, **21** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
