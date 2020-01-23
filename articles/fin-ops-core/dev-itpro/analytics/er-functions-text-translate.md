---
title: TRANSLATE ER işlevi
description: Bu konu, TRANSLATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916718"
---
# <span data-ttu-id="b0124-103"><a name="TRANSLATE">TRANSLATE ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="b0124-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0124-104">`TRANSLATE` işlev, belirtilen metin dizesini bir bütün veya bir kısmı başka bir dizeyle değiştirildikten sonra *dize* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="b0124-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0124-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="b0124-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="b0124-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="b0124-106">Arguments</span></span>

<span data-ttu-id="b0124-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="b0124-107">`text`: *String*</span></span>

<span data-ttu-id="b0124-108">*Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="b0124-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="b0124-109">`pattern`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="b0124-109">`pattern`: *String*</span></span>

<span data-ttu-id="b0124-110">Metnin değiştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0124-110">The text that must be replaced.</span></span>

<span data-ttu-id="b0124-111">`replacement`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="b0124-111">`replacement`: *String*</span></span>

<span data-ttu-id="b0124-112">Yerine konacak metin.</span><span class="sxs-lookup"><span data-stu-id="b0124-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="b0124-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="b0124-113">Return values</span></span>

<span data-ttu-id="b0124-114">*Dize*</span><span class="sxs-lookup"><span data-stu-id="b0124-114">*String*</span></span>

<span data-ttu-id="b0124-115">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="b0124-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b0124-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="b0124-116">Example</span></span>

<span data-ttu-id="b0124-117">`TRANSLATE ("abcdef", "cd", "GH")`, **"cd"** deseni değiştirir, şunun ile: **"GH"** ve bunu döndürür: **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="b0124-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0124-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b0124-118">Additional resources</span></span>

[<span data-ttu-id="b0124-119">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="b0124-119">Text functions</span></span>](er-functions-category-text.md)
