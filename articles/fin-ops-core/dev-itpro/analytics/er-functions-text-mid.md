---
title: MID ER işlevi
description: Bu konu, MID Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744731"
---
# <a name="mid-er-function"></a><span data-ttu-id="08604-103">MID ER işlevi</span><span class="sxs-lookup"><span data-stu-id="08604-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08604-104">Bu `MID` işlev belirtilen pozisyondan başlayarak belirtilen dizenin başından itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="08604-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="08604-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="08604-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="08604-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="08604-106">Arguments</span></span>

<span data-ttu-id="08604-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="08604-107">`text`: *String*</span></span>

<span data-ttu-id="08604-108">Karakterlerin alınacağı metni belirten bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="08604-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="08604-109">`starting position`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="08604-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="08604-110">Belirtilen metinden ilk karakterin döndürülmesi gereken konumu belirten bir *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="08604-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="08604-111">`number of characters`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="08604-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="08604-112">Belirtilen pozisyondan başlayarak döndürülmesi gereken karakter sayısını belirten bir *tamsayı* değeri.</span><span class="sxs-lookup"><span data-stu-id="08604-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="08604-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="08604-113">Return values</span></span>

<span data-ttu-id="08604-114">*Dize*</span><span class="sxs-lookup"><span data-stu-id="08604-114">*String*</span></span>

<span data-ttu-id="08604-115">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="08604-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="08604-116">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="08604-116">Usage notes</span></span>

<span data-ttu-id="08604-117">`starting position` bağımsız değişkenin değeri 0 (sıfır) değerinden küçükse, döndürülen karakterler belirtilen dizedeki ilk konumdan sayılır.</span><span class="sxs-lookup"><span data-stu-id="08604-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="08604-118">`starting position` bağımsız değişkenin değeri belirtilen dizenin uzunluğunu aşarsa, boş bir dize döndürülür.</span><span class="sxs-lookup"><span data-stu-id="08604-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="08604-119">Örnek</span><span class="sxs-lookup"><span data-stu-id="08604-119">Example</span></span>

<span data-ttu-id="08604-120">`MID ("Sample", 2, 3)`, **"amp"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="08604-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08604-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="08604-121">Additional resources</span></span>

[<span data-ttu-id="08604-122">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="08604-122">Text functions</span></span>](er-functions-category-text.md)
