---
title: TRANSLATE ER işlevi
description: Bu konu, TRANSLATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 7e4d6417757e27190ab7cabf2bf01243bb87b55c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746085"
---
# <a name="translate-er-function"></a><span data-ttu-id="64d12-103">TRANSLATE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="64d12-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64d12-104">`TRANSLATE` işlevi, başka bir küme için karakterlerle belirtilen metnin karakter değiştirme sonucunu içeren bir *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="64d12-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d12-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="64d12-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="64d12-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="64d12-106">Arguments</span></span>

<span data-ttu-id="64d12-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="64d12-107">`text`: *String*</span></span>

<span data-ttu-id="64d12-108">*Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="64d12-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="64d12-109">`pattern`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="64d12-109">`pattern`: *String*</span></span>

<span data-ttu-id="64d12-110">Metnin değiştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="64d12-110">The text that must be replaced.</span></span>

<span data-ttu-id="64d12-111">`replacement`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="64d12-111">`replacement`: *String*</span></span>

<span data-ttu-id="64d12-112">Yerine konacak metin.</span><span class="sxs-lookup"><span data-stu-id="64d12-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="64d12-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="64d12-113">Return values</span></span>

<span data-ttu-id="64d12-114">*Dize*</span><span class="sxs-lookup"><span data-stu-id="64d12-114">*String*</span></span>

<span data-ttu-id="64d12-115">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="64d12-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="64d12-116">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="64d12-116">Usage notes</span></span>

<span data-ttu-id="64d12-117">`TRANSLATE` işlevi bir seferde bir karakteri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="64d12-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="64d12-118">İşlev, `text` bağımsız değişkenin ilk karakterini `pattern` bağımsız değişkenin ilk karakteriyle değiştirir, sonra ikinci karakteri değiştirir ve tamamlanana kadar aynı akışla devam eder.</span><span class="sxs-lookup"><span data-stu-id="64d12-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="64d12-119">`text` ve `pattern` bağımsız değişkenlerden bir karakter eşleştiğinde, bu karakter `pattern` bağımsız değişkeninden gelen karakterle aynı konumda bulunan `replacement` bağımsız değişkenden gelen karakter ile değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="64d12-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="64d12-120">Bir karakter `pattern` bağımsız değişkende birden çok kez görünürse, bu karakterin ilk oluşumuna karşılık gelen `replacement` bağımsız değişkeni eşlemesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="64d12-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="64d12-121">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="64d12-121">Example 1</span></span>

<span data-ttu-id="64d12-122">`TRANSLATE ("abcdef", "cd", "GH")` aşağıdaki nedenle, belirtilen **“abcdef”** metninin **"c"** karakterini `replacement` metninin **"G"**  karakteriyle değiştirir:</span><span class="sxs-lookup"><span data-stu-id="64d12-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="64d12-123">**"c"** karakteri ilk konumdaki `pattern` metinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="64d12-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="64d12-124">`replacement` metninin ilk konumu **"G"** karakterini içerir.</span><span class="sxs-lookup"><span data-stu-id="64d12-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="64d12-125">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="64d12-125">Example 2</span></span>

<span data-ttu-id="64d12-126">`TRANSLATE ("abcdef", "ccd", "GH")` **"abGdef"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="64d12-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="64d12-127">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="64d12-127">Example 3</span></span>

<span data-ttu-id="64d12-128">`TRANSLATE ("abccba", "abc", "123")`, **"123321"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="64d12-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64d12-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="64d12-129">Additional resources</span></span>

[<span data-ttu-id="64d12-130">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="64d12-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]