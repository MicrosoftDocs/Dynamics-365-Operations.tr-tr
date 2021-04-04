---
title: TABLENAME2ID ER işlevi
description: Bu konu, TABLENAME2ID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563282"
---
# <a name="tablename2id-er-function"></a>TABLENAME2ID ER işlevi

[!include [banner](../includes/banner.md)]

Bu `TABLENAME2ID` işlevi, belirtilen tablo için tablo kodunun sayısal gösterimini *tamsayı* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Geçerli bir tablo adını gösteren bir metin değeri.

## <a name="return-values"></a>Dönüş değerleri

*Tamsayı*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlevin yürütülmesi, aynı şirket adı kullanılsa bile farklı Microsoft Dynamics 365 Finance örneklerinde farklı sonuçlar elde edebilir.

## <a name="example"></a>Örnek

`TABLENAME2ID ("Intrastat")`, **1510** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]