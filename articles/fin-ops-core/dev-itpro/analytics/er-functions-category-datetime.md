---
title: Tarih ve zaman kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen tarih ve saat işlevleri hakkında bilgi sağlar.
author: NickSelin
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
ms.openlocfilehash: 2dd8524c9cd368f0fe64347e3212b419bb0902b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744573"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="4468d-103">Tarih ve zaman kategorisindeki ER işlevlerinin listesi</span><span class="sxs-lookup"><span data-stu-id="4468d-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4468d-104">Elektronik raporlama (ER) Tarih ve saat işlevleri, tarih ve saat değerlerinden bilgi ayıklamak ve bunlar üzerinde işlem gerçekleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4468d-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="4468d-105">Bu konu, bu işlevlerin özetini sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4468d-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="4468d-106">Desteklenen işlevler listesi</span><span class="sxs-lookup"><span data-stu-id="4468d-106">List of supported functions</span></span>

| <span data-ttu-id="4468d-107">İşlev</span><span class="sxs-lookup"><span data-stu-id="4468d-107">Function</span></span> | <span data-ttu-id="4468d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4468d-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4468d-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="4468d-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="4468d-110">Bu işlev, belirtilen başlangıç tarihinden önceki veya sonraki gün sayısı olan bir *tarih saat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="4468d-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="4468d-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="4468d-112">Bu işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde metin olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="4468d-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4468d-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="4468d-114">Bu işlev, belirli bir tarih/saat değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde metin olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="4468d-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="4468d-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="4468d-116">Bu işlev, belirli bir metin değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde tarih/saat değeri olarak gösteren bir *TarihSaat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="4468d-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="4468d-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="4468d-118">Bu işlev, Eşgüdümlü evrensel saatdeki (Greenwich saati \[GMT\]) belirli bir tarih değerinden bir tarih/saat değerine dönüştürülmüş bir *tarih saat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="4468d-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="4468d-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="4468d-120">Bu işlev, belirli bir metin değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde tarih/saat değeri olarak gösteren bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="4468d-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="4468d-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="4468d-122">Bu işlev, Ocak 1 ve belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="4468d-123">Vade erteleme gün sayısı</span><span class="sxs-lookup"><span data-stu-id="4468d-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="4468d-124">Bu işlev, belirli bir tarihte ve ikinci belirtilen tarih arasındaki günlerin sayısının bir *tamsayı* temsilini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="4468d-125">Now</span><span class="sxs-lookup"><span data-stu-id="4468d-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="4468d-126">Bu işlev, geçerli uygulama sunucusu tarih ve saatini temsil eden bir *TarihSaat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="4468d-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="4468d-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="4468d-128">Bu işlev, **boş** tarihi temsil eden bir *tarih* değeri döndürür (1 Ocak, 1900).</span><span class="sxs-lookup"><span data-stu-id="4468d-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="4468d-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="4468d-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="4468d-130">Bu işlev,eşgüdümlü evrensel saat içinde **boş** tarih/zaman değerini (1 Ocak, 1900) gösteren bir *tarih saat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="4468d-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="4468d-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="4468d-132">Bu işlev, geçerli uygulama oturumu tarih ve saatini temsil eden bir *TarihSaat* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="4468d-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="4468d-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="4468d-134">Bu işlev, geçerli uygulama oturumu tarih temsil eden bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="4468d-135">Bugün</span><span class="sxs-lookup"><span data-stu-id="4468d-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="4468d-136">Bu işlev, geçerli uygulama sunucusu tarih temsil eden bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4468d-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="4468d-137">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4468d-137">Additional resources</span></span>

[<span data-ttu-id="4468d-138">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="4468d-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="4468d-139">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="4468d-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4468d-140">Elektronik raporlamada formül dili</span><span class="sxs-lookup"><span data-stu-id="4468d-140">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]