---
title: Tarih ve zaman kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen tarih ve saat işlevleri hakkında bilgi sağlar.
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916580"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Tarih ve zaman kategorisindeki ER işlevlerinin listesi

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) Tarih ve saat işlevleri, tarih ve saat değerlerinden bilgi ayıklamak ve bunlar üzerinde işlem gerçekleştirmek için kullanılabilir. Bu konu, bu işlevlerin özetini sunmaktadır.

## <a name="list-of-supported-functions"></a>Desteklenen işlevler listesi

| İşlev | Tanım |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Bu işlev, belirtilen başlangıç tarihinden önceki veya sonraki gün sayısı olan bir *tarih saat* değeri döndürür. |
| [DateFormat](er-functions-datetime-dateformat.md) | Bu işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde metin olarak gösteren bir *dize* değeri döndürür. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Bu işlev, belirli bir tarih/saat değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde metin olarak gösteren bir *dize* değeri döndürür. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Bu işlev, belirli bir metin değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde tarih/saat değeri olarak gösteren bir *TarihSaat* değeri döndürür. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Bu işlev, Eşgüdümlü evrensel saatdeki (Greenwich saati \[GMT\]) belirli bir tarih değerinden bir tarih/saat değerine dönüştürülmüş bir *tarih saat* değeri döndürür. |
| [DateValue](er-functions-datetime-datevalue.md) | Bu işlev, belirli bir metin değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde tarih/saat değeri olarak gösteren bir *Tarih* değeri döndürür. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Bu işlev, Ocak 1 ve belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür. |
| [Vade erteleme gün sayısı](er-functions-datetime-days.md) | Bu işlev, belirli bir tarihte ve ikinci belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür. |
| [Now](er-functions-datetime-now.md) | Bu işlev, geçerli uygulama sunucusu tarih ve saatini temsil eden bir *TarihSaat* değeri döndürür. |
| [NullDate](er-functions-datetime-nulldate.md) | Bu işlev, **boş** tarihi temsil eden bir *tarih* değeri döndürür (1 Ocak, 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Bu işlev,eşgüdümlü evrensel saat içinde **boş** tarih/zaman değerini (1 Ocak, 1900) gösteren bir *tarih saat* değeri döndürür. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Bu işlev, geçerli uygulama oturumu tarih ve saatini temsil eden bir *TarihSaat* değeri döndürür. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Bu işlev, geçerli uygulama oturumu tarih temsil eden bir *Tarih* değeri döndürür. |
| [Bugün](er-functions-datetime-today.md) | Bu işlev, geçerli uygulama sunucusu tarih temsil eden bir *Tarih* değeri döndürür. |

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Elektronik raporlamada formül dili](er-formula-language.md)
