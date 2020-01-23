---
title: DATETIMEFORMAT ER işlevi
description: Bu konu, DATETIMEFORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 98919f40751a77465ae26acbd46af4396c588b13
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916419"
---
# <span data-ttu-id="e7ea8-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="e7ea8-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7ea8-104">`DATETIMEFORMAT` işlev, belirli bir tarih/saat değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde metin olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="e7ea8-105">Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="e7ea8-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="e7ea8-106">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="e7ea8-106">Syntax 1</span></span>

```
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="e7ea8-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="e7ea8-107">Syntax 2</span></span>

```
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="e7ea8-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="e7ea8-108">Arguments</span></span>

<span data-ttu-id="e7ea8-109">`datetime`: *TarihSaat*</span><span class="sxs-lookup"><span data-stu-id="e7ea8-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="e7ea8-110">Biçimlendirilecek tarihi ve saati gösteren tarih/saat değeri.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="e7ea8-111">`format`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="e7ea8-111">`format`: *String*</span></span>

<span data-ttu-id="e7ea8-112">Çıkış dizesinin biçimi.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-112">The format of the output string.</span></span>

<span data-ttu-id="e7ea8-113">`culture`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="e7ea8-113">`culture`: *String*</span></span>

<span data-ttu-id="e7ea8-114">Biçimlendirme için kullanılacak kültür.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="e7ea8-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e7ea8-115">Return values</span></span>

<span data-ttu-id="e7ea8-116">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e7ea8-116">*String*</span></span>

<span data-ttu-id="e7ea8-117">Sonuç dize değeri.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e7ea8-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="e7ea8-118">Usage notes</span></span>

<span data-ttu-id="e7ea8-119">Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlandığında, `culture` değeri çağıran bağlam tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="e7ea8-120">Örneğin, `DATETIMEFORMAT` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="e7ea8-121">Varsayılan `culture` değeri **EN-US**'dir.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="e7ea8-122">`DATETIMEFORMAT` işlev verilen bir tarih/saat değerini dönüştürdüğünde, işlevin bağlamında çağrıldığı ER biçimini çalıştıran uygulama kullanıcısının saat dilimi ayarını dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="e7ea8-123">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7ea8-123">Example 1</span></span>

<span data-ttu-id="e7ea8-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarih/saat değerini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="e7ea8-125">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e7ea8-125">Example 2</span></span>

<span data-ttu-id="e7ea8-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarih/saat değerini (24 Aralık 2015) döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="e7ea8-127">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e7ea8-127">Example 3</span></span>

<span data-ttu-id="e7ea8-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")`, Saat dilimi değerine sahip bir uygulama kullanıcısı tarafından başlatılan bir işlem sırasında çağrıldığında **2019-11-12T08:00:00.0000000-08:00** dize değerini döndürür, **dil ve ülke/bölge tercihleri** bölümünde **Eşgüdümlü Evrensel Saat (GMT-08:00) Pasifik Saat (ABD ve Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="e7ea8-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7ea8-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e7ea8-129">Additional resources</span></span>

[<span data-ttu-id="e7ea8-130">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="e7ea8-130">Date and time functions</span></span>](er-functions-category-datetime.md)
