---
title: DATETIMEFORMAT ER işlevi
description: Bu konu, DATETIMEFORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 859753c04e3b3d3b61d9a61edaf396637ed5a003
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746999"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="46720-103">DATETIMEFORMAT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="46720-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46720-104">`DATETIMEFORMAT` işlev, belirli bir tarih/saat değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde metin olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="46720-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="46720-105">Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="46720-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="46720-106">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="46720-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="46720-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="46720-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="46720-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="46720-108">Arguments</span></span>

<span data-ttu-id="46720-109">`datetime`: *TarihSaat*</span><span class="sxs-lookup"><span data-stu-id="46720-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="46720-110">Biçimlendirilecek tarihi ve saati gösteren tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="46720-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="46720-111">`format`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="46720-111">`format`: *String*</span></span>

<span data-ttu-id="46720-112">Çıkış dizesinin biçimi.</span><span class="sxs-lookup"><span data-stu-id="46720-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="46720-113">Standart biçim veya özel biçim kullanırken biçim dizesi büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="46720-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="46720-114">Örneğin, [standart](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" biçim tanımlayıcısı kısa tarih modelini kullanarak tarihi döndürürken standart "D" biçim tanımlayıcısı uzun tarih modelini kullanarak tarihi döndürür.</span><span class="sxs-lookup"><span data-stu-id="46720-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="46720-115">Ek olarak, [özel](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" biçim tanımlayıcısı 1 ile 12 arasındaki ayları döndürürken özel "m" biçim tanımlayıcısı 0 ile 59 arasındaki dakikaları döndürür.</span><span class="sxs-lookup"><span data-stu-id="46720-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="46720-116">`culture`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="46720-116">`culture`: *String*</span></span>

<span data-ttu-id="46720-117">Biçimlendirme için kullanılacak kültür.</span><span class="sxs-lookup"><span data-stu-id="46720-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="46720-118">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="46720-118">Return values</span></span>

<span data-ttu-id="46720-119">*Dize*</span><span class="sxs-lookup"><span data-stu-id="46720-119">*String*</span></span>

<span data-ttu-id="46720-120">Sonuç dize değeri.</span><span class="sxs-lookup"><span data-stu-id="46720-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="46720-121">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="46720-121">Usage notes</span></span>

<span data-ttu-id="46720-122">Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlanmamışsa `culture` değeri, çağıran bağlam tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="46720-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="46720-123">Örneğin, `DATETIMEFORMAT` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="46720-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="46720-124">Varsayılan `culture` değeri **EN-US**'dir.</span><span class="sxs-lookup"><span data-stu-id="46720-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="46720-125">`DATETIMEFORMAT` işlev verilen bir tarih/saat değerini dönüştürdüğünde, işlevin bağlamında çağrıldığı ER biçimini çalıştıran uygulama kullanıcısının saat dilimi ayarını dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="46720-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="46720-126">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="46720-126">Example 1</span></span>

<span data-ttu-id="46720-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarih/saat değerini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="46720-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="46720-128">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="46720-128">Example 2</span></span>

<span data-ttu-id="46720-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarih/saat değerini (24 Aralık 2015) döndürür.</span><span class="sxs-lookup"><span data-stu-id="46720-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="46720-130">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="46720-130">Example 3</span></span>

<span data-ttu-id="46720-131">İşlev, **Dil ve ülke/bölge tercihleri** bölümünde saat dilimi değeri **(GMT-08:00) Pasifik Saati (ABD ve Kanada)** olan bir uygulama kullanıcı tarafından başlatılan işlem sırasında çağrıldığında `DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")`, **2019-11-12T08:00:00.0000000-08:00** dize değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="46720-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46720-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="46720-132">Additional resources</span></span>

[<span data-ttu-id="46720-133">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="46720-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]