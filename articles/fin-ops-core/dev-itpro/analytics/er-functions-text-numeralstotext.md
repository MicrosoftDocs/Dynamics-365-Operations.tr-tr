---
title: NUMERALSTOTEXT ER işlev işlevi
description: Bu konu, NUMERALSTOTEXT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: e26890a0d99e0df631a3b3350d284e63aaed8e09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746159"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="dc048-103">NUMERALSTOTEXT ER işlev işlevi</span><span class="sxs-lookup"><span data-stu-id="dc048-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc048-104">Bu `NUMERALSTOTEXT` işlevi belirtilen sayıyı bir *dize* değeri olarak (metin dizelerine dönüştürüldükten sonra) belirtilen dilde yazılmış şekilde döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc048-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc048-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="dc048-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="dc048-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="dc048-106">Arguments</span></span>

<span data-ttu-id="dc048-107">`number`: *Tamsayı* veya *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="dc048-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="dc048-108">Yazılması gereken sayıyı belirten sayısal değer.</span><span class="sxs-lookup"><span data-stu-id="dc048-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="dc048-109">`language`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="dc048-109">`language`: *String*</span></span>

<span data-ttu-id="dc048-110">dil kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="dc048-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="dc048-111">`currency`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="dc048-111">`currency`: *String*</span></span>

<span data-ttu-id="dc048-112">Para birimi kodunu temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="dc048-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="dc048-113">`print currency name flag`: *Boole*</span><span class="sxs-lookup"><span data-stu-id="dc048-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="dc048-114">Yazılmış metne bir para birimi adının eklenip eklenmeyeceğini belirten bir *Boole* değeri.</span><span class="sxs-lookup"><span data-stu-id="dc048-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="dc048-115">`decimal points`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="dc048-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="dc048-116">Yazılmış metinde sahip olması gereken ondalık basamak sayısını gösteren bir *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="dc048-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="dc048-117">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="dc048-117">Return values</span></span>

<span data-ttu-id="dc048-118">*Dize*</span><span class="sxs-lookup"><span data-stu-id="dc048-118">*String*</span></span>

<span data-ttu-id="dc048-119">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="dc048-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="dc048-120">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="dc048-120">Usage notes</span></span>

<span data-ttu-id="dc048-121">Dil kodu isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="dc048-121">The language code is optional.</span></span> <span data-ttu-id="dc048-122">Boş dize olarak tanımlandığında, çalışma bağlamının dil kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc048-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="dc048-123">Varsayılan dil değeri kodu **tr-tr**'dir.</span><span class="sxs-lookup"><span data-stu-id="dc048-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="dc048-124">Çalışan bağlamın dil kodu, çalışmakta olan elektronik raporlama (ER ) biçiminin bir **klasöründe** veya **dosya** öğesinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="dc048-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="dc048-125">Para birimi kodu isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="dc048-125">The currency code is optional.</span></span> <span data-ttu-id="dc048-126">Boş dize olarak tanımlandığında, çalışma bağlamının şirket para birimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc048-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="dc048-127">`print currency name flag` ve `decimal points` bağımsız değişkenleri, para birimi adını yazdır bayrağı ve ondalık basamak parametreleri yalnızca şu dil kodları için analiz edilir: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** ve **RU**.</span><span class="sxs-lookup"><span data-stu-id="dc048-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="dc048-128">Ek olarak, `print currency name flag` bağımsız değişkeni yalnızca ülke veya bölge bağlamının para birimi adlarının gerilemesini destekleyen şirketler için analiz edilir.</span><span class="sxs-lookup"><span data-stu-id="dc048-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="dc048-129">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dc048-129">Example 1</span></span>

<span data-ttu-id="dc048-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)`, **"Bin İki Yüz Otuz Dört ve 56"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc048-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="dc048-131">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dc048-131">Example 2</span></span>

<span data-ttu-id="dc048-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)`, **"Sto dwadzieścia"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc048-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="dc048-133">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="dc048-133">Example 3</span></span>

<span data-ttu-id="dc048-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)`, **"Сто двадцать евро 21 евроцент"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="dc048-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc048-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="dc048-135">Additional resources</span></span>

[<span data-ttu-id="dc048-136">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="dc048-136">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]