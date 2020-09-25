---
title: LISTJOIN ER işlevi
description: Bu konu, LISTJOIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 035bf720a892e987ff9fc073ab8ed6f6cc6ea18e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745117"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER işlevi

[!include [banner](../includes/banner.md)]

`LISTJOIN` işlevi, belirtilen bağımsız değişkenlerden oluşturulmuş yeni birleştirilmiş kayıt listesini temsil eden yeni bir *Kayıt listesi* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Bağımsız değişkenler

`list 1`: *Kayıt listesi*

*Kayıt listesi* veri türünün veri kaynağına yönelik referans. Bu bağımsız değişken zorunlu.

`list N`: *Kayıt listesi*

*Kayıt listesi* veri türünün veri kaynağına yönelik referans. Bu ek bağımsız değişkenler isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Oluşturulan listenin yapısı, yalnızca bağımsız değişkenlerde başvurulan her kayıt listesinin yapısında sunulan alanları içerir.

## <a name="example"></a>Örnek

`Container` türünün veri kaynağı **Kayıt 1**'i girersiniz. Bu veri kaynağı, `Calculated field` türünün aşağıdaki iç içe geçmiş alanlarını içerir:

- **Kod**: Bu alan, `String` türünde bir değer döndüren bir ifade içerir.
- **Tutar**: Bu alan, `Real` türünde bir değer döndüren bir ifade içerir.

Sonra, `Container` türünün veri kaynağı **Kayıt 2**'yi girersiniz. Bu veri kaynağı, `Calculated field` türünün aşağıdaki iç içe geçmiş alanlarını içerir:

- **Tutar**: Bu alan, `Real` türünde bir değer döndüren bir ifade içerir.
- **IsValid**: Bu alan, `Boolean` türünde bir değer döndüren bir ifade içerir.

![ER model eşleme tasarımcısı sayfası](./media/er-functions-list-listjoin-image1.gif)

Bu durumda, `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` ifade iki kayıt içeren yeni bir liste döndürür.

![İki kayıt bulunan ER model eşleme tasarımcısı sayfası](./media/er-functions-list-listjoin-image2.gif)

Bu listenin yapısı, bu alan çağrılan işlevin her bir bağımsız değişkeninde sunulan tek alan olduğundan, `Real` türününü tek bir **Tutar** alanından oluşur.

![ER model eşleme tasarımcısı sayfası miktar alanı](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)

[Veri akışı ve dönüşümünü analiz etmek için yürütülen bir ER biçiminin veri kaynaklarında hata ayıklama](er-debug-data-sources.md)
