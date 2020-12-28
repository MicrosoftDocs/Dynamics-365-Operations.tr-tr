---
title: DATEVALUE ER işlevi
description: Bu konu, DATEVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 43e65055b0803ed330a19568f9565c3fae488ab2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682425"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="aadfa-103">DATEVALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="aadfa-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aadfa-104">`DATEVALUE` işlev, belirli bir metin değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde tarih/saat değeri olarak gösteren bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="aadfa-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="aadfa-105">Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="aadfa-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="aadfa-106">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="aadfa-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="aadfa-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="aadfa-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="aadfa-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="aadfa-108">Arguments</span></span>

<span data-ttu-id="aadfa-109">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="aadfa-109">`text`: *String*</span></span>

<span data-ttu-id="aadfa-110">Biçimlendirilecek değeri gösteren bir metin değeri.</span><span class="sxs-lookup"><span data-stu-id="aadfa-110">Text that represents the value to format.</span></span>

<span data-ttu-id="aadfa-111">`format`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="aadfa-111">`format`: *String*</span></span>

<span data-ttu-id="aadfa-112">Belirli metnin biçimi.</span><span class="sxs-lookup"><span data-stu-id="aadfa-112">The format of the given text.</span></span>

<span data-ttu-id="aadfa-113">`culture`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="aadfa-113">`culture`: *String*</span></span>

<span data-ttu-id="aadfa-114">Verilen metnin biçimlendirilmesi için kullanılan kültür.</span><span class="sxs-lookup"><span data-stu-id="aadfa-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="aadfa-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="aadfa-115">Return values</span></span>

<span data-ttu-id="aadfa-116">*Tarih*</span><span class="sxs-lookup"><span data-stu-id="aadfa-116">*Date*</span></span>

<span data-ttu-id="aadfa-117">Sonuç tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="aadfa-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="aadfa-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="aadfa-118">Usage notes</span></span>

<span data-ttu-id="aadfa-119">Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlandığında, `culture` değeri çağıran bağlam tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="aadfa-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="aadfa-120">Örneğin, `DATEVALUE` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="aadfa-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="aadfa-121">Varsayılan `culture` değeri **EN-US**'dir.</span><span class="sxs-lookup"><span data-stu-id="aadfa-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="aadfa-122">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aadfa-122">Example 1</span></span>

<span data-ttu-id="aadfa-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")`, belirtilen özel biçim ve varsayılan uygulamanın **en-US** kültürü temelinde **21 Aralık 2016** tarih değeri arasında bir değer verir.</span><span class="sxs-lookup"><span data-stu-id="aadfa-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="aadfa-124">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="aadfa-124">Example 2</span></span>

<span data-ttu-id="aadfa-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")`, belirtilen özel biçime ve kültüre dayalı olarak **21Ocak 2016** Tarih değerlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="aadfa-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="aadfa-126">Bununla birlikte, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` belirtilen dizenin geçerli bir tarih olarak tanınmadığını kullanıcıya bildirmek için bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aadfa-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aadfa-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="aadfa-127">Additional resources</span></span>

[<span data-ttu-id="aadfa-128">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="aadfa-128">Date and time functions</span></span>](er-functions-category-datetime.md)
