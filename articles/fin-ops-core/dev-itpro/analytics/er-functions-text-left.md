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
ms.openlocfilehash: 4293db244d04debf3679cf2bde0b892bd74e8ead
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041136"
---
# <span data-ttu-id="cf48e-103"><a name="LEFT">LEFT ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="cf48e-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf48e-104">Bu `LEFT` işlev belirtilen dizenin başından itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf48e-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf48e-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="cf48e-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="cf48e-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="cf48e-106">Arguments</span></span>

<span data-ttu-id="cf48e-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="cf48e-107">`text`: *String*</span></span>

<span data-ttu-id="cf48e-108">Orijinal metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="cf48e-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="cf48e-109">`number`: *Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="cf48e-109">`number`: *Integer*</span></span>

<span data-ttu-id="cf48e-110">Orijinal metnin başından itibaren döndürülmesi gereken karakter sayısı.</span><span class="sxs-lookup"><span data-stu-id="cf48e-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="cf48e-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="cf48e-111">Return values</span></span>

<span data-ttu-id="cf48e-112">*Dize*</span><span class="sxs-lookup"><span data-stu-id="cf48e-112">*String*</span></span>

<span data-ttu-id="cf48e-113">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="cf48e-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="cf48e-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="cf48e-114">Example</span></span>

<span data-ttu-id="cf48e-115">`LEFT ("Sample", 3)`, **"Sam"** döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf48e-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf48e-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cf48e-116">Additional resources</span></span>

[<span data-ttu-id="cf48e-117">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="cf48e-117">Text functions</span></span>](er-functions-category-text.md)
