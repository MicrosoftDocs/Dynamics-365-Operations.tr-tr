---
title: GETENUMVALUEBYNAME işlevi
description: Bu konu, GETENUMVALUEBYNAME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916856"
---
# <a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME işlevi</a>

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME` işlevi, belirtilen numaralandırma veri kaynağındaki belirli bir *Enum* değerini *dize* değeri olarak belirtilen numaralandırma adını kullanarak arar. *Numaralama* değeri bulunursa, işlev bunu döndürür. Aksi durumda, işlev **boş** numaralandırma değerini döndürür.

## <a name="syntax"></a>Sözdizimi

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`enumeration data source path`: *numaralandırması*

Aşağıdaki sabit listesi tiplerinden birinin veri kaynağının geçerli yolu:

- Elektronik raporlama (ER) model numaralandırması
- ER biçim numaralandırma
- Microsoft Dynamics 365 Finance numaralandırması

`enumeration value text`: *Dize*

Tek bir numaralandırma değerinin adını gösteren bir dize değeri.

## <a name="return-values"></a>Dönüş değerleri

Boş giriş yapılabilir *Enum*

Sonuç numaralandırma değeri.

## <a name="usage-notes"></a>Kullanım notları

Bir *dize* değeri olarak belirtilen numaralandırma değerinin adı kullanılarak bir *Enum* değeri bulunamazsa, hiçbir özel durum atılır.

## <a name="example"></a>Örnek

Aşağıdaki örnekte, bir veri modelinde oluşturulan **ReportDirection** numaralandırması gösterilmektedir. Etiketlerin numaralandırma değerleri ile tanımlandığını unutmayın.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Aşağıdaki örnek ayrıntıları göstermektedir:

- **$Direction** veri kaynağı bir er raporu içinde konfigüre edilmiş. Bu veri kaynağı **RaporYönü** modeli sabit listesi temel alınarak yapılandırıldı.
- Bu işlevin parametresi olarak model numaralandırmaya dayalı **$Direction** veri kaynağı kullanmak için tasarlanan `$IsArrivals` ifadesi.
- Bu karşılaştırma ifadenin değeri **DOĞRU**'dur.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)
