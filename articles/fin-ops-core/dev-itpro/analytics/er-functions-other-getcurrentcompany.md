---
title: GETCURRENTCOMPANY ER işlevi
description: Bu makalede, GETCURRENTCOMPANY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b5f5f7d7c884000f59b93e10875f78289a879779
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280200"
---
# <a name="getcurrentcompany-er-function"></a>GETCURRENTCOMPANY ER işlevi

[!include [banner](../includes/banner.md)]

`GETCURRENTCOMPANY` işlevi, bir kullanıcının oturum açmış olduğu tüzel kişiliğin (şirket) kodunu temsil eden *Dize* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example"></a>Örnek

`GETCURRENTCOMPANY ()`, **Contoso Entertainment System USA** şirketinde oturum açmış bir kullanıcı için **USMF** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
