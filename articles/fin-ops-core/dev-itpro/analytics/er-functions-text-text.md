---
title: TEXT ER işlevi
description: Bu konu, TEXT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 0694480f5d6892d13fe0c0d9ad191cdf2332dfec
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746111"
---
# <a name="text-er-function"></a>TEXT ER işlevi

[!include [banner](../includes/banner.md)]

`TEXT` işlevi, belirtilen giriş geçerli uygulama örneğinin sunucu yerel ayarlarına göre biçimlendirilmiş bir metin dizesine çevrildikten sonra bleirtilen sayıyı *dize* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
TEXT (number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Tamsayı* veya *Gerçek*

Bir metin dizesine dönüştürülmesi gereken sayı değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

*Gerçek* türün değerleri için, dize dönüşümü iki ondalık basamakla sınırlıdır.

## <a name="example"></a>Örnek

Microsoft Dynamics 365 Finance örneğinin sunucu yerel ayarı **EN-US** olarak tanımlanırsa, `TEXT (NOW ())` geçerli Finance oturum tarihi olan Aralık 17, 2015 değerini **"12/17/2015 07:59:23 AM"** metin dizesi olarak döndürür. `TEXT (1/3)`, **"0.33"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]