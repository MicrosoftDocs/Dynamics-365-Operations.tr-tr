---
title: CHAR ER işlevi
description: Bu konu, CHAR Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041251"
---
# <a name="CHAR">CHAR ER işlevi</a>

[!include [banner](../includes/banner.md)]

Bu `CHAR` işlev, belirtilen Unicode sayısı tarafından başvurulan tek bir karakteri gösteren bir *dize* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
CHAR (number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Tamsayı*

Beklenen tek bir karaktere karşılık gelen sayı.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlevin döndürdüğü dize **DOSYA** biçimi üst öğesinde seçtiğiniz kodlamaya bağlıdır. Desteklenen kodlamalar listesi için bkz. [Kodlama sınıfı](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Örnek

`CHAR (255)`, **"ÿ"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)
