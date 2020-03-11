---
title: TEXT ER işlevi
description: Bu konu, TEXT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: c08aca949ffc7e62009bf3f6c664d96b368f43e7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040910"
---
# <a name="TEXT">TEXT ER işlevi</a>

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
