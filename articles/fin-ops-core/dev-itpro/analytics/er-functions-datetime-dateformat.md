---
title: DATEFORMAT ER işlevi
description: Bu konu, DATEFORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: c1453be0c93764f9f0364206822a9e3899061a58
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917592"
---
# <a name="DATEFORMAT">DATEFORMAT ER işlevi</a>

[!include [banner](../includes/banner.md)]

`DATEFORMAT` işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde metin olarak gösteren bir *dize* değeri döndürür. Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Sözdizimi 1

```
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Sözdizimi 2

```
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Bağımsız değişkenler

`date`: *Tarih*

Biçimlendirilecek tarihi gösteren bir tarih değeri.

`format`: *Dize*

Çıkış dizesinin biçimi.

`culture`: *Dize*

Biçimlendirme için kullanılacak kültür.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç dize değeri.

## <a name="usage-notes"></a>Kullanım notları

Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlandığında, `culture` değeri çağıran bağlam tarafından tanımlanır. Örneğin, `DATEFORMAT` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır. Varsayılan `culture` değeri **EN-US**'dir.

## <a name="example-1"></a>Örnek 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarihini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.

## <a name="example-2"></a>Örnek 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarihini (24 Aralık 2015) döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)