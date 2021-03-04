---
title: CONVERTCURRENCY ER işlevi
description: Bu konu, CONVERTCURRENCY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: a27fd30236a61576ab9063010ea6bc38d9cf7a1e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686798"
---
# <a name="convertcurrency-er-function"></a>CONVERTCURRENCY ER işlevi

[!include [banner](../includes/banner.md)]

`CONVERTCURRENCY` işlev, belirtilen parasal tutarı kaynak para biriminden, belirtilen tarihte belirtilen şirketinin ayarlarını kullanarak belirtilen hedef para birimine dönüştürme sonucunu temsil eden *Gerçek* değer döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Bağımsız değişkenler

`amount`: *Tamsayı* veya *Gerçek*

Dönüştürülmesi gereken parasal tutarı gösteren sayısal değer.

`source currency`: *Dize*

Kaynak para birimi kodu.

`target currency`: *Dize*

Hedef para birimi kodu.

`date`: *Tarih*

Dönüştürme için Döviz kurunu belirlemek amacıyla kullanılan tarihi temsil eden bir *tarih* değeri.

`company`: *Dize*

Dönüştürme için kullanılan ayarları sağlayan şirketin kodunu temsil eden bir *dize* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Gerçek*

Sonuç sayısal değeri.

## <a name="example"></a>Örnek

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")`, şimdiki oturum tarihinde, **DEMF** şirket ayarlarına dayalı olarak bir euro'nun ABD doları olarak karşılığını döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]