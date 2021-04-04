---
title: FORMATELEMENTNAME ER işlevi
description: Bu konu, FORMATELEMENTNAME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561314"
---
# <a name="formatelementname-er-function"></a>FORMATELEMENTNAME ER işlevi

[!include [banner](../includes/banner.md)]

`FORMATELEMENTNAME` işlev, geçerli ER biçim öğesinin adını gösteren bir *Dize* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlev, ER biçimi bileşeninin **toplanan veri anahtarı adı** ve **Toplanan veri anahtarı değeri** özelliği için yapılandırılmış ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan **metin** grubundan çağrılabilir.

## <a name="example"></a>Örnek

Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için [ER Sayma ve toplama için çıktı biçiminde verileri kullanma](tasks/er-format-counting-summing-1.md) görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun.

## <a name="additional-resources"></a>Ek kaynaklar

[Veri toplama işlevleri](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]