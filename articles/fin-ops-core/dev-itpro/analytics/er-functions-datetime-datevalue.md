---
title: DATEVALUE ER işlevi
description: Bu konu, DATEVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: d760c3f874bfebad11b9497b136cb67df4e9ea61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746951"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="db97b-103">DATEVALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="db97b-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db97b-104">`DATEVALUE` işlev, belirli bir metin değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde tarih/saat değeri olarak gösteren bir *Tarih* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="db97b-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="db97b-105">Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="db97b-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="db97b-106">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="db97b-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="db97b-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="db97b-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="db97b-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="db97b-108">Arguments</span></span>

<span data-ttu-id="db97b-109">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="db97b-109">`text`: *String*</span></span>

<span data-ttu-id="db97b-110">Biçimlendirilecek değeri gösteren bir metin değeri.</span><span class="sxs-lookup"><span data-stu-id="db97b-110">Text that represents the value to format.</span></span>

<span data-ttu-id="db97b-111">`format`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="db97b-111">`format`: *String*</span></span>

<span data-ttu-id="db97b-112">Belirli metnin biçimi.</span><span class="sxs-lookup"><span data-stu-id="db97b-112">The format of the given text.</span></span>

<span data-ttu-id="db97b-113">`culture`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="db97b-113">`culture`: *String*</span></span>

<span data-ttu-id="db97b-114">Verilen metnin biçimlendirilmesi için kullanılan kültür.</span><span class="sxs-lookup"><span data-stu-id="db97b-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="db97b-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="db97b-115">Return values</span></span>

<span data-ttu-id="db97b-116">*Tarih*</span><span class="sxs-lookup"><span data-stu-id="db97b-116">*Date*</span></span>

<span data-ttu-id="db97b-117">Sonuç tarih değeri.</span><span class="sxs-lookup"><span data-stu-id="db97b-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="db97b-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="db97b-118">Usage notes</span></span>

<span data-ttu-id="db97b-119">Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlandığında, `culture` değeri çağıran bağlam tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="db97b-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="db97b-120">Örneğin, `DATEVALUE` işlev, Almanca kültür kullanacak şekilde konfigüre edilen bir **DOSYA** öğesi için elektronik raporlama (er) biçiminde bir sözdizimi 1 kullanılarak çağrılırsa, dönüştürme işlemi Almanca kültür kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="db97b-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="db97b-121">Varsayılan `culture` değeri **EN-US**'dir.</span><span class="sxs-lookup"><span data-stu-id="db97b-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="db97b-122">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="db97b-122">Example 1</span></span>

<span data-ttu-id="db97b-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")`, belirtilen özel biçim ve varsayılan uygulamanın **en-US** kültürü temelinde **21 Aralık 2016** tarih değeri arasında bir değer verir.</span><span class="sxs-lookup"><span data-stu-id="db97b-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="db97b-124">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="db97b-124">Example 2</span></span>

<span data-ttu-id="db97b-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")`, belirtilen özel biçime ve kültüre dayalı olarak **21Ocak 2016** Tarih değerlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="db97b-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="db97b-126">Bununla birlikte, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` belirtilen dizenin geçerli bir tarih olarak tanınmadığını kullanıcıya bildirmek için bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db97b-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db97b-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="db97b-127">Additional resources</span></span>

[<span data-ttu-id="db97b-128">Tarih ve saat işlevleri</span><span class="sxs-lookup"><span data-stu-id="db97b-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]