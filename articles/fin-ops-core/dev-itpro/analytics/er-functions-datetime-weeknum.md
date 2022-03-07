---
title: WEEKNUM ER işlevi
description: Bu konu, WEEKNUM Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/03/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: fe36d4142b6e4922e2cbca09bb0ca9f68f6680a0
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891351"
---
# <a name="weeknum-er-function"></a>WEEKNUM ER işlevi

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

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
