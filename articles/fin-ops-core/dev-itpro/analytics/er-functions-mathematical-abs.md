---
title: ABS ER işlevi
description: Bu konu, ABS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041665"
---
# <a name="ABS">ABS ER işlevi</a>

[!include [banner](../includes/banner.md)]

`ABS` işlev, belirtilen sayının mutlak değeri (katsayı) bir *Gerçek* değer olarak döndürür. Diğer bir deyişle, işareti olmadan sayıyı döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ABS (number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Gerçek*

Modülü bir mod olmasını istediğiniz sayısal değer.

## <a name="return-values"></a>Dönüş değerleri

*Gerçek*

Sonuç sayısal değeri.

## <a name="example"></a>Örnek

`ABS (-1)`, **1** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Matematik işlevi](er-functions-category-mathematical.md)
