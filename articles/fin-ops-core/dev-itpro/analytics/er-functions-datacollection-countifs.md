---
title: COUNTIFS ER işlevi
description: Bu konu, COUNTIFS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 02e401254cdfebd4b549f63dbd6a5f925e7bf544
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916488"
---
# <a name="COUNTIFS">COUNTIFS ER işlevi</a>

[!include [banner](../includes/banner.md)]

`COUNTIFS` işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşula uyuyan Biçim öğelerinin sayısını temsil eden bir *tamsayı* değer döndürür. Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.

## <a name="syntax"></a>Sözdizimi

```
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Bağımsız değişkenler

`condition 1 range`: *Dize*

Bir elektronik raporlama (ER) biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer. Bu bağımsız değişken zorunlu.

`condition 1 value`: *Dize*

Bir ER biçim bileşeninin **toplanan veri anahtarı değeri** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer. Bu bağımsız değişken zorunlu.

`condition N range`: *Dize*

Bir ER biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer. Bu ek bağımsız değişkenler isteğe bağlıdır.

`condition N value`: *Dize*

Bir ER biçim bileşeninin **toplanan veri anahtarı değeri** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer. Bu ek bağımsız değişkenler isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Tamsayı*

Sonuç sayısal değeri.

## <a name="usage-notes"></a>Kullanım notları

Bu işlev, **toplanan veri anahtarı adı** ve **Toplanan veri anahtarı değeri** özelliği, ER biçimi bileşeninin **Sıra** bileşeni veya **XML Öğesi** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.

Bu işlev, Geçerli **Ortak\\Dosya** bileşeninin **Çıkış ayrıntılarını topla** seçeneği bayrağı kapatıldığında **0** (sıfır) değeri döner.

`condition range` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.

`condition value` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.

## <a name="example"></a>Örnek

Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için [ER Sayma ve toplama için çıktı biçiminde verileri kullanma](tasks/er-format-counting-summing-1.md) görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun.

## <a name="additional-resources"></a>Ek kaynaklar

[Veri toplama işlevleri](er-functions-category-data-collection.md)