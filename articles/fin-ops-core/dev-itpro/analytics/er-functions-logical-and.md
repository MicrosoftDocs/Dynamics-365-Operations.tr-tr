---
title: AND ER işlevi
description: Bu konu, AND Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 4a246496eca0d5a8538ac7f1577957e6b9eae4e3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743484"
---
# <a name="and-er-function"></a>AND ER işlevi

[!include [banner](../includes/banner.md)]

Belirtilen koşulların tümü doğru ise, `AND` işlev *Boole* **DOĞRU** değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Bağımsız değişkenler

`condition 1`: *Boole*

Test işlem uygulanacak geçerli bir koşullu ifade. Bu bağımsız değişken gereklidir.

`condition N`: *Boole*

Test işlem uygulanacak geçerli bir koşullu ifade. Bu ek bağımsız değişkenler isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Boole*

Sonuç *Boole* değeri.

## <a name="usage-notes"></a>Kullanım notları

Mantıksal işlevlerin bağımsız değişkenlerinde, veri kaynağı başvurularını, sayısal ve metin değerlerini, Boole değerlerini, karşılaştırma işleçlerini ve diğer elektronik raporlama (ER) işlevlerini kullanabilirsiniz. Ancak , tüm bağımsız değişkenlerin **doğru** veya **yanlış** *Boole* değeriyle değerlendirilmesi gerekir.

## <a name="example"></a>Örnek

`AND (1=1, "a"="a")`, **DOĞRU** döndürür.

`AND (1=2, "a"="a")`, **YANLIŞ** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Mantıksal işlevler](er-functions-category-logical.md)
