---
title: NUMBERFORMAT ER işlevi
description: Bu konu, NUMBERFORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 8de57d8b0a45b8b58849a24f2d8f0cde41e0ea3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746230"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="b1442-103">NUMBERFORMAT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="b1442-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1442-104">`NUMBERFORMAT` işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen [kültür](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) içinde belirtilen sayıyı gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="b1442-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="b1442-105">Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="b1442-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b1442-106">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="b1442-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="b1442-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="b1442-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="b1442-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="b1442-108">Arguments</span></span>

<span data-ttu-id="b1442-109">`number`: *Tamsayı* veya *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="b1442-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="b1442-110">Biçimlendirilmesi gereken sayıyı belirten sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="b1442-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="b1442-111">`format`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="b1442-111">`format` : *String*</span></span>

<span data-ttu-id="b1442-112">Biçimi temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="b1442-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="b1442-113">`culture`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="b1442-113">`culture`: *String*</span></span>

<span data-ttu-id="b1442-114">Biçimlendirme için kullanılacak kültürü temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="b1442-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1442-115">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="b1442-115">Return values</span></span>

<span data-ttu-id="b1442-116">*Dize*</span><span class="sxs-lookup"><span data-stu-id="b1442-116">*String*</span></span>

<span data-ttu-id="b1442-117">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="b1442-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b1442-118">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="b1442-118">Usage notes</span></span>

<span data-ttu-id="b1442-119">Kültür çağrılan işlevin bağımsız değişkeni olarak tanımlanmamışsa, bu işlevin çalıştırıldığı bağlam numaraları biçimlendirmek için kullanılan kültürü belirler.</span><span class="sxs-lookup"><span data-stu-id="b1442-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="b1442-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b1442-120">Example 1</span></span>

<span data-ttu-id="b1442-121">**TR-TR** kültürü için `NUMBERFORMAT (0.45, "p")` **"% 45.00"** ve `NUMBERFORMAT (10.45, "#")`, **"10"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="b1442-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b1442-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b1442-122">Example 2</span></span>

<span data-ttu-id="b1442-123">`NUMBERFORMAT (10/3, "F2", "de")`, **3,33**; `NUMBERFORMAT (10/3, "F2", "en-us")`, **3.33** döndürür.</span><span class="sxs-lookup"><span data-stu-id="b1442-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1442-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b1442-124">Additional resources</span></span>

[<span data-ttu-id="b1442-125">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="b1442-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]