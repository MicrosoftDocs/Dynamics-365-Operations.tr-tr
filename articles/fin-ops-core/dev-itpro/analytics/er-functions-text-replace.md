---
title: REPLACE ER işlevi
description: Bu konu, REPLACE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: c9e64bd8e039b4eeca829c3c37299f002ba03592
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743748"
---
# <a name="replace-er-function"></a><span data-ttu-id="2c50a-103">REPLACE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="2c50a-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c50a-104">`REPLACE` işlev, belirtilen metin dizesini bir bütün veya bir kısmı başka bir dizeyle değiştirildikten sonra *dize* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c50a-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c50a-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="2c50a-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="2c50a-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="2c50a-106">Arguments</span></span>

<span data-ttu-id="2c50a-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="2c50a-107">`text`: *String*</span></span>

<span data-ttu-id="2c50a-108">*Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="2c50a-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="2c50a-109">`pattern`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="2c50a-109">`pattern`: *String*</span></span>

<span data-ttu-id="2c50a-110">`regular expression flag` Bağımsız değişken, **yanlış** ise, bu bağımsız değişken değiştirilmesi gereken metni içerir.</span><span class="sxs-lookup"><span data-stu-id="2c50a-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="2c50a-111">`regular expression flag` Bağımsız değişken **doğru** ise, bu bağımsız değişken hem arama desenini hem de yerine konacak metni tanımlayan normal bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="2c50a-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="2c50a-112">`replacement`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="2c50a-112">`replacement`: *String*</span></span>

<span data-ttu-id="2c50a-113">`regular expression flag` Bağımsız değişken, **yanlış** ise, bu bağımsız değişken yerine geçecek olarak kullanılan metni içerir.</span><span class="sxs-lookup"><span data-stu-id="2c50a-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="2c50a-114">`regular expression flag` Bağımsız değişken **doğru** ise, bu bağımsız değişken kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="2c50a-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="2c50a-115">`regular expression flag`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="2c50a-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="2c50a-116">Değişiklik yapmak için normal bir ifadenin kullanılmış olup olmadığını gösteren *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="2c50a-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c50a-117">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="2c50a-117">Return values</span></span>

<span data-ttu-id="2c50a-118">*Dize*</span><span class="sxs-lookup"><span data-stu-id="2c50a-118">*String*</span></span>

<span data-ttu-id="2c50a-119">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="2c50a-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2c50a-120">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="2c50a-120">Usage notes</span></span>

<span data-ttu-id="2c50a-121">`regular expression flag` bağımsız değişken **doğru** ise, `pattern` bağımsız değişken tarafından belirtilen normal ifade uygulanarak bu işlev belirtilen dizeyi değiştirildikten sonra döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c50a-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="2c50a-122">Bu düzenli ifade, değiştirilmesi gereken karakterleri bulmakta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2c50a-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="2c50a-123">`regular expression flag` bağımsız değişkeni **FALSE** ise, bu işlev `pattern` bağımsız değişkeninde tanımlanan karakter kümesin `replacement` bağımsız değişkeninin karakterleriyle değiştirildikten sonra belirtilen dizeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c50a-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="2c50a-124">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c50a-124">Example 1</span></span>

<span data-ttu-id="2c50a-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)`, tüm sayısal olmayan karakterleri kaldıran bir normal ifade uygular ve **"19234564971"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c50a-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="2c50a-126">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2c50a-126">Example 2</span></span>

<span data-ttu-id="2c50a-127">`REPLACE ("abcdef", "cd", "GH", false)`, **"cd"** deseni değiştirir, şunun ile: **"GH"** ve bunu döndürür: **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="2c50a-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c50a-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2c50a-128">Additional resources</span></span>

[<span data-ttu-id="2c50a-129">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="2c50a-129">Text functions</span></span>](er-functions-category-text.md)
