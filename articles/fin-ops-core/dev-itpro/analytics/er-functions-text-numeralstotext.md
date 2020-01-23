---
title: NUMERALSTOTEXT ER işlev işlevi
description: Bu konu, NUMERALSTOTEXT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 459123a66dae7a3d87a22b042e1be6585959ac15
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915637"
---
# <a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER işlev işlevi</a>

[!include [banner](../includes/banner.md)]

Bu `NUMERALSTOTEXT` işlevi belirtilen sayıyı bir *dize* değeri olarak (metin dizelerine dönüştürüldükten sonra) belirtilen dilde yazılmış şekilde döndürür.

## <a name="syntax"></a>Sözdizimi

```
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number`: *Tamsayı* veya *Gerçek*

Yazılması gereken sayıyı belirten sayısal değer.

`language`: *Dize*

dil kodunu temsil eden bir *dize* değeri.

`currency`: *Dize*

Para birimi kodunu temsil eden bir *dize* değeri.

`print currency name flag`: *Boole*

Yazılmış metne bir para birimi adının eklenip eklenmeyeceğini belirten bir *Boole* değeri.

`decimal points`: *Tamsayı*

Yazılmış metinde sahip olması gereken ondalık basamak sayısını gösteren bir *tamsayı* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

Dil kodu isteğe bağlıdır. Boş dize olarak tanımlandığında, çalışma bağlamının dil kodu kullanılır. Varsayılan dil değeri kodu **tr-tr**'dir. Çalışan bağlamın dil kodu, çalışmakta olan elektronik raporlama (ER ) biçiminin bir **klasöründe** veya **dosya** öğesinde tanımlanır.

Para birimi kodu isteğe bağlıdır. Boş dize olarak tanımlandığında, çalışma bağlamının şirket para birimi kullanılır.

> [!NOTE] 
> `print currency name flag` ve `decimal points` bağımsız değişkenleri, para birimi adını yazdır bayrağı ve ondalık basamak parametreleri yalnızca şu dil kodları için analiz edilir: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** ve **RU**. Ek olarak, `print currency name flag` bağımsız değişkeni yalnızca ülke veya bölge bağlamının para birimi adlarının gerilemesini destekleyen şirketler için analiz edilir.

## <a name="example-1"></a>Örnek 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)`, **"Bin İki Yüz Otuz Dört ve 56"** döndürür.

## <a name="example-2"></a>Örnek 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)`, **"Sto dwadzieścia"** döndürür. 

## <a name="example-3"></a>Örnek 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)`, **"Сто двадцать евро 21 евроцент"** döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)