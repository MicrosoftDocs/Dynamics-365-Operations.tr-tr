---
title: NULLDATETIME ER işlevi
description: Bu konu, NULLDATETIME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 3cd4c152d4e220a2f6315265ed5e44d148134279
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042282"
---
# <a name="NULLDATETIME">NULLDATETIME ER işlevi</a>

[!include [banner](../includes/banner.md)]

`NULLDATETIME` işlev,eşgüdümlü evrensel saat (Greenwich Saati \[GMT\]) içinde **boş** tarih/zaman değerini (1 Ocak, 1900) gösteren bir *tarih saat* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Dönüş değerleri

*DateTime*

Sonuç tarih/saat değeri.

## <a name="example"></a>Örnek

`DATETIMEFORMAT( NULLDATETIME(), "O")`, Saat dilimi değerine sahip bir uygulama kullanıcısı tarafından başlatılan bir işlem sırasında çağrıldığında **1900-01-01T 00:00:00.0000000+00:00** dize değerini döndürür, **dil ve ülke/bölge tercihleri** bölümünde **Eşgüdümlü Evrensel Saat** (GMT).

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)
