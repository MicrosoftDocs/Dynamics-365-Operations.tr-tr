---
title: DATEFORMAT ER işlevi
description: Bu konu, DATEFORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 1b3a0a2608328b233004034f7ab2ccfa833c17e3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890922"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="b656d-103">DATEFORMAT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="b656d-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b656d-104">`DATEFORMAT` işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde metin olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="b656d-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="b656d-105">Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](/dotnet/standard/base-types/standard-date-and-time-format-strings) ve [özel](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="b656d-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b656d-106">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="b656d-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="b656d-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="b656d-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="b656d-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="b656d-108">Arguments</span></span>

<span data-ttu-id="b656d-109">`date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="b656d-109">`date`: *Date*</span></span>

<span data-ttu-id="b656d-110">Biçimlendirilecek tarihi gösteren bir tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="b656d-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="b656d-111">`format`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="b656d-111">`format`: *String*</span></span>

<span data-ttu-id="b656d-112">Çıkış dizesinin biçimi.</span><span class="sxs-lookup"><span data-stu-id="b656d-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="b656d-113">Standart biçim veya özel biçim kullanırken biçim dizesi büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="b656d-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="b656d-114">Örneğin, [standart](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" biçim tanımlayıcısı kısa tarih modelini kullanarak tarihi döndürürken standart "D" biçim tanımlayıcısı uzun tarih modelini kullanarak tarihi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b656d-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="b656d-115">Ek olarak, [özel](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" biçim tanımlayıcısı 1 ile 12 arasındaki ayları döndürürken özel "m" biçim tanımlayıcısı 0 ile 59 arasındaki dakikaları döndürür.</span><span class="sxs-lookup"><span data-stu-id="b656d-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="b656d-116">`culture`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="b656d-116">`culture`: *String*</span></span>

<span data-ttu-id="b656d-117">Biçimlendirme için kullanılacak kültür.</span><span class="sxs-lookup"><span data-stu-id="b656d-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="b656d-118">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="b656d-118">Return values</span></span>

<span data-ttu-id="b656d-119">*Dize*</span><span class="sxs-lookup"><span data-stu-id="b656d-119">*String*</span></span>

<span data-ttu-id="b656d-120">Sonuç dize değeri.</span><span class="sxs-lookup"><span data-stu-id="b656d-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b656d-121">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="b656d-121">Usage notes</span></span>

<span data-ttu-id="b656d-122">Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlanmamışsa `culture` değeri, çağıran bağlam tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="b656d-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="b656d-123">Örneğin, `DATEFORMAT` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="b656d-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="b656d-124">Varsayılan `culture` değeri **EN-US**'dir.</span><span class="sxs-lookup"><span data-stu-id="b656d-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="b656d-125">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b656d-125">Example 1</span></span>

<span data-ttu-id="b656d-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarihini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="b656d-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="b656d-127">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b656d-127">Example 2</span></span>

<span data-ttu-id="b656d-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarihini (24 Aralık 2015) döndürür.</span><span class="sxs-lookup"><span data-stu-id="b656d-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b656d-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b656d-129">Additional resources</span></span>

[<span data-ttu-id="b656d-130">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="b656d-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]