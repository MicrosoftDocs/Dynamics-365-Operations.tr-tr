---
title: Veri toplama kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen veri toplama işlevleri hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba3a1f031a4a98592081b04a4128450aeb8218ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561746"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>Veri toplama kategorisindeki ER işlevlerinin listesi

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) veri toplama işlevleri, daha önce **metin** veya **XML** biçiminde oluşturulmuş çıktının verilerine dayalı olarak, çalıştırılmakta olan bir er biçimini saymak ve toplamak için kullanılır. Bu yaklaşım, çalıştırılan bir ER biçiminin performansını artırmaya yardımcı olmak, oluşturulan belgelerde çalışan toplam değerleri girmek ve başka amaçlar için kullanılır. Bu konu, bu işlevlerin özetini sunmaktadır.

## <a name="list-of-supported-functions"></a>Desteklenen işlevler listesi

| İşlev | Tanım |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Bu işlev, bir biçim öğesi için **toplanan veri anahtarı değeri** özelliği tarafından döndürülen ve Format ögeleri çalıştırma biçimi sırasında ve belirtilen koşullara uyan bir giden belge oluşturmak için kullanıldığında toplanan değerlerin listesini içeren bir *kayıt listesi* değeri döndürür. Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur. |
| [CountIF](er-functions-datacollection-countif.md) | Bu işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşula uyuyan Biçim öğelerinin sayısını temsil eden bir *tamsayı* değer döndürür. Koşul bir anahtar aralığı ve bir anahtar değerinden oluşur. |
| [CountIFs](er-functions-datacollection-countifs.md) | Bu işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşullara uyuyan Biçim öğelerinin sayısını temsil eden bir *tamsayı* değer döndürür. Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Bu işlev, geçerli ER biçim öğesinin adını gösteren bir *Dize* değeri döndürür. |
| [SumIF](er-functions-datacollection-sumif.md) | Bu işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşula uyuyan Biçim öğelerinin sayısını temsil eden bir *Gerçek* değer döndürür. Koşul bir anahtar aralığı ve bir anahtar değerinden oluşur. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Bu işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşullara uyuyan Biçim öğelerinin sayısını temsil eden bir *Gerçek* değer döndürür. Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur. |

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Elektronik raporlamada formül dili](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]