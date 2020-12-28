---
title: DATEFORMAT ER işlevi
description: Bu konu, DATEFORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fa6bdef2168112aeb17e0edb9f9a6d1b3bd45c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684950"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="700cc-103">DATEFORMAT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="700cc-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="700cc-104">`DATEFORMAT` işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde metin olarak gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="700cc-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="700cc-105">Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="700cc-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="700cc-106">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="700cc-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="700cc-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="700cc-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="700cc-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="700cc-108">Arguments</span></span>

<span data-ttu-id="700cc-109">`date`: *Tarih*</span><span class="sxs-lookup"><span data-stu-id="700cc-109">`date`: *Date*</span></span>

<span data-ttu-id="700cc-110">Biçimlendirilecek tarihi gösteren bir tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="700cc-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="700cc-111">`format`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="700cc-111">`format`: *String*</span></span>

<span data-ttu-id="700cc-112">Çıkış dizesinin biçimi.</span><span class="sxs-lookup"><span data-stu-id="700cc-112">The format of the output string.</span></span>

<span data-ttu-id="700cc-113">`culture`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="700cc-113">`culture`: *String*</span></span>

<span data-ttu-id="700cc-114">Biçimlendirme için kullanılacak kültür.</span><span class="sxs-lookup"><span data-stu-id="700cc-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="700cc-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="700cc-115">Return values</span></span>

<span data-ttu-id="700cc-116">*Dize*</span><span class="sxs-lookup"><span data-stu-id="700cc-116">*String*</span></span>

<span data-ttu-id="700cc-117">Sonuç dize değeri.</span><span class="sxs-lookup"><span data-stu-id="700cc-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="700cc-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="700cc-118">Usage notes</span></span>

<span data-ttu-id="700cc-119">Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlandığında, `culture` değeri çağıran bağlam tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="700cc-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="700cc-120">Örneğin, `DATEFORMAT` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="700cc-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="700cc-121">Varsayılan `culture` değeri **EN-US**'dir.</span><span class="sxs-lookup"><span data-stu-id="700cc-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="700cc-122">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="700cc-122">Example 1</span></span>

<span data-ttu-id="700cc-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` Aralık 24, 2015 olan uygulama sunucusu tarihini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="700cc-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="700cc-124">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="700cc-124">Example 2</span></span>

<span data-ttu-id="700cc-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")`, seçilen Almanca kültür ve belirtilen biçime dayalı olarak, **"24-12-2015"** dizesi olarak geçerli uygulama oturum tarihini (24 Aralık 2015) döndürür.</span><span class="sxs-lookup"><span data-stu-id="700cc-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="700cc-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="700cc-126">Additional resources</span></span>

[<span data-ttu-id="700cc-127">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="700cc-127">Date and time functions</span></span>](er-functions-category-datetime.md)
