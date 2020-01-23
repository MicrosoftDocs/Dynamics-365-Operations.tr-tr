---
title: LIST ER işlevi
description: Bu konu, LIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917293"
---
# <a name="LIST">LIST ER işlevi</a>

[!include [banner](../includes/banner.md)]

`LIST` işlevi, belirtilen bağımsız değişkenlerden oluşturulmuş yeni listeden oluşan yeni bir *kayıt listesi* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Bağımsız değişkenler

`record 1`: *Konteyner (kayıt)*

*Kayıt* veri türünün veri kaynağına yönelik referans. Bu bağımsız değişken gereklidir.

`record N`: *Konteyner (kayıt)*

*Kayıt* veri türünün veri kaynağına yönelik referans. Bu ek bağımsız değişkenler isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Oluşturulan listenin yapısı, yalnızca bağımsız değişkenlerde belirtilen her kaydın yapısında sunulan alanları içerir.

## <a name="example"></a>Örnek

**Konteyner** türünün veri kaynağı *kayıt 1*'i girersiniz. Bu veri kaynağı, *hesaplanan alan* türünün Aşağıdaki iç içe alanlarını içerir:

- **Kod:** Bu alan, *dize* türünde bir değer döndüren bir ifade içerir.
- **Tutar:** Bu alan, *Gerçek* türünde bir değer döndüren bir ifade içerir.

**Konteyner** türünün veri kaynağı *kayıt 2*'i girersiniz. Bu veri kaynağı, *hesaplanan alan* türünün Aşağıdaki iç içe alanlarını içerir:

- **Tutar:** Bu alan, *Gerçek* türünde bir değer döndüren bir ifade içerir.
- **IsValid:** Bu alan, *Boole* türünde bir değer döndüren bir ifade içerir.

Bu durumda, `LIST('Record 1', 'Record 2')` ifade iki kayıt içeren yeni bir liste döndürür. Bu listenin yapısı, bu alan, çağrılan işlevin her bir bağımsız değişkeninde sunulan tek alan olduğundan, *gerçek* türün tek bir **tutar** alanından oluşur.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)