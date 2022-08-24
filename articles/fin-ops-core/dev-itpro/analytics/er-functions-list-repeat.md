---
title: REPEAT ER işlevi
description: Bu makalede, REPEAT Elektronik raporlama (ER) işlevinin nasıl kullanılacağı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220702"
---
# <a name="repeat-er-function"></a>REPEAT ER işlevi

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`REPEAT` işlevi, belirtilen girişle eşleşen bir değeri olan alanı içeren bir kayıt oluşturur. Sonra, belirtilen sayıda yinelenen bir kaydın yeni *Kayıt listesini* döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Bağımsız değişkenler

`item`: Desteklenen herhangi bir [temel](er-formula-supported-data-types-primitive.md) veya [bileşik](er-formula-supported-data-types-composite.md) veri türü

Tekrarlanacak değer.

`number`: *Tamsayı*

Tekrarlama sayısı.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Döndürülen tekrarlanan kayıtların listesi aşağıdaki alanları sunar:

- Belirtilen değer (`Item` alanı)
- Geçerli kayıt dizini (`Number` alanı)

> [!NOTE]
> Bu işlev için tek tabanlı numaralandırma kullanıldığından, `Number` alanı sonuçta ortaya çıkan listenin ilk kaydı için **1** değerine sahip olur.

[Regression Suite Automation Tool'u (RSAT)](../perf-test/rsat/rsat-overview.md) kullanarak [Elektronik raporlama (ER)](general-electronic-reporting.md) çözümlerinin performans ve toplu testlerini yapabilmeniz için varolan verileri çarpmak amacıyla bu işlevi kullanabilirsiniz.

## <a name="example"></a>Örnek

Bir ER biçiminin yürütmesi başlamadan önce çalışma zamanında iletişim kutusundaki bir veri girişi alanında belirttiğiniz kadar çok sayıda `Party` XML öğesi içermesi gereken, XML biçiminde bir belge oluşturmak istiyorsunuz.

Aşağıdaki örnekte ER [biçimi](er-overview-components.md#format-component) gösterilmiştir. Bu biçimde, tek bir tarafın özelliklerini göstermek için tek `Party` XML öğesi eklenir.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Sonraki resim, aşağıdaki yapılandırılan veri kaynaklarını göstermektedir:

- Tek bir tarafı temsil eden `Party` veri kaynağı. `Party.Value` alanı tek bir metin değerini göstermek için kullanılır.
- Oluşturulan belgeye girilmesi gereken tarafların sayısını belirtebilmeniz için çalışma zamanında iletişim kutusunda bir veri girişi alanı sunmak için kullanılan `NumberOfRepeats` [veri kaynağı](er-user-input-parameter-data-sources.md).
- `Party` kaydını `NumberOfRepeats` veri kaynağında belirttiğiniz sayı kadar tekrarlayan `Party2` veri kaynağı.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Sonraki şekil, XML biçiminde çıktı oluşturmak için oluşturulan düzenlenebilir ER biçiminin veri bağlamalarını gösterir. Bu çıktı ayrı ayrı tarafları numaralandırılmış düğümler olarak gösterir.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Aşağıdaki şekil, tasarlanan biçim çalıştırıldığında ve `NumberOfRepeats` veri kaynağının değeri **5** olarak belirtildiğinde ortaya çıkan sonucu gösterir.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
