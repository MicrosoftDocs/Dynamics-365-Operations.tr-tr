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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 112852ab955fdf8de9f78cc93486cc1d5f048517
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743795"
---
# <a name="left-er-function"></a><span data-ttu-id="450b4-103">LEFT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="450b4-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="450b4-104">Bu `LEFT` işlev belirtilen dizenin başından itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="450b4-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="450b4-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="450b4-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="450b4-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="450b4-106">Arguments</span></span>

<span data-ttu-id="450b4-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="450b4-107">`text`: *String*</span></span>

<span data-ttu-id="450b4-108">Orijinal metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="450b4-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="450b4-109">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="450b4-109">`number`: *Integer*</span></span>

<span data-ttu-id="450b4-110">Orijinal metnin başından itibaren döndürülmesi gereken karakter sayısı.</span><span class="sxs-lookup"><span data-stu-id="450b4-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="450b4-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="450b4-111">Return values</span></span>

<span data-ttu-id="450b4-112">*Dize*</span><span class="sxs-lookup"><span data-stu-id="450b4-112">*String*</span></span>

<span data-ttu-id="450b4-113">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="450b4-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="450b4-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="450b4-114">Example</span></span>

<span data-ttu-id="450b4-115">`LEFT ("Sample", 3)`, **"Sam"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="450b4-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="450b4-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="450b4-116">Additional resources</span></span>

[<span data-ttu-id="450b4-117">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="450b4-117">Text functions</span></span>](er-functions-category-text.md)
