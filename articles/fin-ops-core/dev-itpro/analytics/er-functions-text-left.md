---
title: LEFT ER işlevi
description: Bu konu, LEFT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685895"
---
# <a name="left-er-function"></a><span data-ttu-id="e6cbc-103">LEFT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="e6cbc-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6cbc-104">Bu `LEFT` işlev belirtilen dizenin başından itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6cbc-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6cbc-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e6cbc-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="e6cbc-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="e6cbc-106">Arguments</span></span>

<span data-ttu-id="e6cbc-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="e6cbc-107">`text`: *String*</span></span>

<span data-ttu-id="e6cbc-108">Orijinal metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="e6cbc-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="e6cbc-109">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="e6cbc-109">`number`: *Integer*</span></span>

<span data-ttu-id="e6cbc-110">Orijinal metnin başından itibaren döndürülmesi gereken karakter sayısı.</span><span class="sxs-lookup"><span data-stu-id="e6cbc-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="e6cbc-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e6cbc-111">Return values</span></span>

<span data-ttu-id="e6cbc-112">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e6cbc-112">*String*</span></span>

<span data-ttu-id="e6cbc-113">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="e6cbc-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e6cbc-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="e6cbc-114">Example</span></span>

<span data-ttu-id="e6cbc-115">`LEFT ("Sample", 3)`, **"Sam"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6cbc-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6cbc-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e6cbc-116">Additional resources</span></span>

[<span data-ttu-id="e6cbc-117">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="e6cbc-117">Text functions</span></span>](er-functions-category-text.md)
